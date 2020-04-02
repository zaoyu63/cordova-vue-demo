<style lang="scss">
  .img {
    text-align: center;
  }

  .zt-button {
    display: inline-block;
    line-height: 1;
    white-space: nowrap;
    cursor: pointer;
    background: #fff;
    border: 1px solid #dcdfe6;
    color: #606266;
    -webkit-appearance: none;
    text-align: center;
    box-sizing: border-box;
    outline: none;
    margin: 0;
    transition: .1s;
    font-weight: 500;
    -moz-user-select: none;
    -webkit-user-select: none;
    -ms-user-select: none;
    padding: 12px 20px;
    font-size: 14px;
    border-radius: 4px;
    width: 100%;

    &.is-primary {
      color: #fff;
      background-color: #409eff;
      border-color: #409eff;
    }

    &.is-success {
      color: #fff;
      background-color: #67c23a;
      border-color: #67c23a;
    }
    &.is-info {
      color: #fff;
      background-color: #909399;
      border-color: #909399;
    }
    &.is-warn {
      color: #fff;
      background-color: #e6a23c;
      border-color: #e6a23c;
    }
    &.is-danger {
      color: #fff;
      background-color: #f56c6c;
      border-color: #f56c6c;
    }
  }

  .mb-10 {
    margin-bottom: 10px;
  }
</style>
<template>
  <div class="home">
    <div class="img">
      <img alt="Vue logo" src="../assets/logo.png">
    </div>
    <div class="mb-10">
      <button class="zt-button is-primary" @click="camera">相机</button>
    </div>
    <div class="mb-10">
      <button class="zt-button is-success" @click="scan">二维码</button>
    </div>
    <div class="mb-10">
      <button class="zt-button is-info" @click="call">打电话</button>
    </div>
  </div>
</template>

<script>

  import {Camera} from '@ionic-native/camera/ngx';
  import {BarcodeScanner} from '@ionic-native/barcode-scanner/ngx';
  import {CallNumber} from '@ionic-native/call-number/ngx';
  export default {
    name: 'home',
    methods: {
      camera() {
        const camera = new Camera();
        const CameraOptions = {
          quality: 100,
          destinationType: camera.DestinationType.FILE_URI,
          encodingType: camera.EncodingType.JPEG,
          mediaType: camera.MediaType.PICTURE
        };
        camera.getPicture(CameraOptions).then();
      },
      scan() {
        const barcodeScanner = new BarcodeScanner();
        barcodeScanner.scan().then(barcodeData => {
          console.log('Barcode data', barcodeData);
        }).catch(err => {
          console.log('Error', err);
        });
      },
      call() {
        const callNumber = new CallNumber();
        callNumber.callNumber('10086', true)
          .then(res => console.log('Launched dialer!', res))
          .catch(err => console.log('Error launching dialer', err));
      }
    }
  };
</script>

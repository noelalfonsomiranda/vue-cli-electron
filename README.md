// vue.config.js

module.exports = {
  lintOnSave: false,
  pluginOptions: {
    electronBuilder: {
      chainWebpackRendererProcess: config => {
        if (process.env.NODE_ENV === 'development') {
          config.devServer.port('3000')
        }
      }
    }
  }
}

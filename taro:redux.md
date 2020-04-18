action: 调用redux（就是调用接口，或调用本地的reducer）
reducer： 缓存数据或者缓存后端返回的数据

调用方式：
action中
export const userInfo = (payload) => ({
  type: XXX,
  payload
})

reducer中
case XXX:{
  ...state,
  userInfo: { ...action.payload }
} 

接口数据是调用action中定义的接口函数。this.props.dispatchGetLogin()
保存数据到reducer中，this.props.userInfo({idCard, name})

获取reducer中保存在本地的userInfo： const { idCard, name } = this.props.userInfo

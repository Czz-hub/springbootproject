<template>
	<div class="addEdit-block" :style='{"minHeight":"100vh","padding":"30px 30px 30px 0","fontSize":"14px","color":"#666","background":"#f4f8fb"}'>
		<el-form
			:style='{"border":"1px solid #e1e8ee","padding":"50px 10% 20px","overflow":"hidden","borderRadius":"0px","alignItems":"flex-start","flexWrap":"wrap","background":"rgba(255,255,255,1)","display":"flex","fontSize":"inherit"}'
			class="add-update-preview"
			ref="ruleForm"
			:model="ruleForm"
			:rules="rules"
			label-width="180px"
		>
			<template >
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' class="input" v-if="type!='info'"  label="食物名称" prop="shiwumingcheng">
					<el-input v-model="ruleForm.shiwumingcheng" placeholder="食物名称" clearable  :readonly="ro.shiwumingcheng"></el-input>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' v-else class="input" label="食物名称" prop="shiwumingcheng">
					<el-input v-model="ruleForm.shiwumingcheng" placeholder="食物名称" readonly></el-input>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' class="input" v-if="type!='info'"  label="蛋白质" prop="danbaizhi">
					<el-input-number v-model="ruleForm.danbaizhi" placeholder="蛋白质" :disabled="ro.danbaizhi"></el-input-number>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' v-else class="input" label="蛋白质" prop="danbaizhi">
					<el-input v-model="ruleForm.danbaizhi" placeholder="蛋白质" readonly></el-input>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' class="input" v-if="type!='info'"  label="脂肪" prop="zhifang">
					<el-input-number v-model="ruleForm.zhifang" placeholder="脂肪" :disabled="ro.zhifang"></el-input-number>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' v-else class="input" label="脂肪" prop="zhifang">
					<el-input v-model="ruleForm.zhifang" placeholder="脂肪" readonly></el-input>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' class="input" v-if="type!='info'"  label="碳水化合物" prop="tanshuihuahewu">
					<el-input-number v-model="ruleForm.tanshuihuahewu" placeholder="碳水化合物" :disabled="ro.tanshuihuahewu"></el-input-number>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' v-else class="input" label="碳水化合物" prop="tanshuihuahewu">
					<el-input v-model="ruleForm.tanshuihuahewu" placeholder="碳水化合物" readonly></el-input>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' class="input" v-if="type!='info'"  label="膳食纤维" prop="shanshixianwei">
					<el-input-number v-model="ruleForm.shanshixianwei" placeholder="膳食纤维" :disabled="ro.shanshixianwei"></el-input-number>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' v-else class="input" label="膳食纤维" prop="shanshixianwei">
					<el-input v-model="ruleForm.shanshixianwei" placeholder="膳食纤维" readonly></el-input>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' class="input" v-if="type!='info'"  label="热量" prop="reliang">
					<el-input-number v-model="ruleForm.reliang" placeholder="热量" :disabled="ro.reliang"></el-input-number>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' v-else class="input" label="热量" prop="reliang">
					<el-input v-model="ruleForm.reliang" placeholder="热量" readonly></el-input>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' class="input" v-if="type!='info'"  label="维生素" prop="weishengsu">
					<el-input-number v-model="ruleForm.weishengsu" placeholder="维生素" :disabled="ro.weishengsu"></el-input-number>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' v-else class="input" label="维生素" prop="weishengsu">
					<el-input v-model="ruleForm.weishengsu" placeholder="维生素" readonly></el-input>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' class="upload" v-if="type!='info' && !ro.shiwutupian" label="食物图片" prop="shiwutupian">
					<file-upload
						tip="点击上传食物图片"
						action="file/upload"
						:limit="3"
						:multiple="true"
						:fileUrls="ruleForm.shiwutupian?ruleForm.shiwutupian:''"
						@change="shiwutupianUploadChange"
					></file-upload>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' class="upload" v-else-if="ruleForm.shiwutupian" label="食物图片" prop="shiwutupian">
					<img v-if="ruleForm.shiwutupian.substring(0,4)=='http'" class="upload-img" style="margin-right:20px;" v-bind:key="index" :src="ruleForm.shiwutupian.split(',')[0]" width="100" height="100">
					<img v-else class="upload-img" style="margin-right:20px;" v-bind:key="index" v-for="(item,index) in ruleForm.shiwutupian.split(',')" :src="$base.url+item" width="100" height="100">
				</el-form-item>
			</template>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' v-if="type!='info'"  label="相关信息" prop="xiangguanxinxi">
					<editor 
						style="min-width: 200px; max-width: 600px;"
						v-model="ruleForm.xiangguanxinxi" 
						class="editor" 
						action="file/upload">
					</editor>
				</el-form-item>
				<el-form-item :style='{"border":"0px solid #eee","padding":"0","margin":"0 0 20px 0","color":"inherit","borderRadius":"0px","display":"inline-block","width":"100%","fontSize":"inherit"}' v-else-if="ruleForm.xiangguanxinxi" label="相关信息" prop="xiangguanxinxi">
                    <span :style='{"fontSize":"14px","lineHeight":"40px","minWidth":"1000px","color":"inherit","fontWeight":"500","display":"inline-block"}' v-html="ruleForm.xiangguanxinxi"></span>
                </el-form-item>
			<el-form-item :style='{"padding":"10px 0 20px","margin":"30px 0","alignItems":"center","textAlign":"left","display":"block","width":"100%","clear":"both","perspective":"320px","-webkitPerspective":"320px","fontSize":"48px","justifyContent":"flex-start"}' class="btn">
				<el-button class="btn3"  v-if="type!='info'" type="success" @click="onSubmit">
					<span class="icon iconfont icon-tijiao16" :style='{"margin":"0 2px","fontSize":"18px","color":"inherit","display":"none"}'></span>
					保存
				</el-button>
				<el-button class="btn4" v-if="type!='info'" type="success" @click="back()">
					<span class="icon iconfont icon-quxiao09" :style='{"margin":"0 2px","fontSize":"18px","color":"inherit","display":"none"}'></span>
					取消
				</el-button>
				<el-button class="btn5" v-if="type=='info'" type="success" @click="back()">
					<span class="icon iconfont icon-fanhui01" :style='{"margin":"0 2px","fontSize":"18px","color":"inherit","display":"none"}'></span>
					返回
				</el-button>
			</el-form-item>
		</el-form>
    

  </div>
</template>
<script>
import { 
	isNumber,
} from "@/utils/validate";
export default {
	data() {
		var validateNumber = (rule, value, callback) => {
			if(!value){
				callback();
			} else if (!isNumber(value)) {
				callback(new Error("请输入数字"));
			} else {
				callback();
			}
		};
		return {
			id: '',
			type: '',
			
			
			ro:{
				shiwumingcheng : false,
				danbaizhi : false,
				zhifang : false,
				tanshuihuahewu : false,
				shanshixianwei : false,
				reliang : false,
				weishengsu : false,
				xiangguanxinxi : false,
				shiwutupian : false,
			},
			
			
			ruleForm: {
				shiwumingcheng: '',
				danbaizhi: '',
				zhifang: '',
				tanshuihuahewu: '',
				shanshixianwei: '',
				reliang: '',
				weishengsu: '',
				xiangguanxinxi: '',
				shiwutupian: '',
			},
		

			
			rules: {
				shiwumingcheng: [
				],
				danbaizhi: [
					{ validator: validateNumber, trigger: 'blur' },
				],
				zhifang: [
					{ validator: validateNumber, trigger: 'blur' },
				],
				tanshuihuahewu: [
					{ validator: validateNumber, trigger: 'blur' },
				],
				shanshixianwei: [
					{ validator: validateNumber, trigger: 'blur' },
				],
				reliang: [
					{ validator: validateNumber, trigger: 'blur' },
				],
				weishengsu: [
					{ validator: validateNumber, trigger: 'blur' },
				],
				xiangguanxinxi: [
				],
				shiwutupian: [
				],
			}
		};
	},
	props: ["parent"],
	computed: {



	},
    components: {
    },
	created() {
	},
	methods: {
		
		// 下载
		download(file){
			window.open(`${file}`)
		},
		// 初始化
		init(id,type) {
			if (id) {
				this.id = id;
				this.type = type;
			}
			if(this.type=='info'||this.type=='else'){
				this.info(id);
			}else if(this.type=='logistics'){
				this.logistics=false;
				this.info(id);
			}else if(this.type=='cross'){
				var obj = this.$storage.getObj('crossObj');
				for (var o in obj){
						if(o=='shiwumingcheng'){
							this.ruleForm.shiwumingcheng = obj[o];
							this.ro.shiwumingcheng = true;
							continue;
						}
						if(o=='danbaizhi'){
							this.ruleForm.danbaizhi = obj[o];
							this.ro.danbaizhi = true;
							continue;
						}
						if(o=='zhifang'){
							this.ruleForm.zhifang = obj[o];
							this.ro.zhifang = true;
							continue;
						}
						if(o=='tanshuihuahewu'){
							this.ruleForm.tanshuihuahewu = obj[o];
							this.ro.tanshuihuahewu = true;
							continue;
						}
						if(o=='shanshixianwei'){
							this.ruleForm.shanshixianwei = obj[o];
							this.ro.shanshixianwei = true;
							continue;
						}
						if(o=='reliang'){
							this.ruleForm.reliang = obj[o];
							this.ro.reliang = true;
							continue;
						}
						if(o=='weishengsu'){
							this.ruleForm.weishengsu = obj[o];
							this.ro.weishengsu = true;
							continue;
						}
						if(o=='xiangguanxinxi'){
							this.ruleForm.xiangguanxinxi = obj[o];
							this.ro.xiangguanxinxi = true;
							continue;
						}
						if(o=='shiwutupian'){
							this.ruleForm.shiwutupian = obj[o];
							this.ro.shiwutupian = true;
							continue;
						}
				}
			}
			// 获取用户信息
			this.$http({
				url: `${this.$storage.get('sessionTable')}/session`,
				method: "get"
			}).then(({ data }) => {
				if (data && data.code === 0) {
					var json = data.data;
				} else {
					this.$message.error(data.msg);
				}
			});
			
		},
    // 多级联动参数

    info(id) {
      this.$http({
        url: `shiwuyingyang/info/${id}`,
        method: "get"
      }).then(({ data }) => {
        if (data && data.code === 0) {
        this.ruleForm = data.data;
        //解决前台上传图片后台不显示的问题
        let reg=new RegExp('../../../upload','g')//g代表全部
        this.ruleForm.xiangguanxinxi = this.ruleForm.xiangguanxinxi.replace(reg,'../../../springbootc0as852x/upload');
        } else {
          this.$message.error(data.msg);
        }
      });
    },


    // 提交
    onSubmit() {
	if(this.ruleForm.shiwutupian!=null) {
		this.ruleForm.shiwutupian = this.ruleForm.shiwutupian.replace(new RegExp(this.$base.url,"g"),"");
	}
var objcross = this.$storage.getObj('crossObj');
      //更新跨表属性
       var crossuserid;
       var crossrefid;
       var crossoptnum;
       if(this.type=='cross'){
                var statusColumnName = this.$storage.get('statusColumnName');
                var statusColumnValue = this.$storage.get('statusColumnValue');
                if(statusColumnName!='') {
                        var obj = this.$storage.getObj('crossObj');
                       if(statusColumnName && !statusColumnName.startsWith("[")) {
                               for (var o in obj){
                                 if(o==statusColumnName){
                                   obj[o] = statusColumnValue;
                                 }
                               }
                               var table = this.$storage.get('crossTable');
                             this.$http({
                                 url: `${table}/update`,
                                 method: "post",
                                 data: obj
                               }).then(({ data }) => {});
                       } else {
                               crossuserid=this.$storage.get('userid');
                               crossrefid=obj['id'];
                               crossoptnum=this.$storage.get('statusColumnName');
                               crossoptnum=crossoptnum.replace(/\[/,"").replace(/\]/,"");
                        }
                }
        }
		this.$refs["ruleForm"].validate(valid => {
			if (valid) {
				if(crossrefid && crossuserid) {
					this.ruleForm.crossuserid = crossuserid;
					this.ruleForm.crossrefid = crossrefid;
					let params = { 
						page: 1, 
						limit: 10, 
						crossuserid:this.ruleForm.crossuserid,
						crossrefid:this.ruleForm.crossrefid,
					} 
				this.$http({ 
					url: "shiwuyingyang/page", 
					method: "get", 
					params: params 
				}).then(({ 
					data 
				}) => { 
					if (data && data.code === 0) { 
						if(data.data.total>=crossoptnum) {
							this.$message.error(this.$storage.get('tips'));
							return false;
						} else {
							this.$http({
								url: `shiwuyingyang/${!this.ruleForm.id ? "save" : "update"}`,
								method: "post",
								data: this.ruleForm
							}).then(({ data }) => {
								if (data && data.code === 0) {
									this.$message({
										message: "操作成功",
										type: "success",
										duration: 1500,
										onClose: () => {
											this.parent.showFlag = true;
											this.parent.addOrUpdateFlag = false;
											this.parent.shiwuyingyangCrossAddOrUpdateFlag = false;
											this.parent.search();
											this.parent.contentStyleChange();
										}
									});
								} else {
									this.$message.error(data.msg);
								}
							});

						}
					} else { 
				} 
			});
		} else {
			this.$http({
				url: `shiwuyingyang/${!this.ruleForm.id ? "save" : "update"}`,
				method: "post",
			   data: this.ruleForm
			}).then(({ data }) => {
				if (data && data.code === 0) {
					this.$message({
						message: "操作成功",
						type: "success",
						duration: 1500,
						onClose: () => {
							this.parent.showFlag = true;
							this.parent.addOrUpdateFlag = false;
							this.parent.shiwuyingyangCrossAddOrUpdateFlag = false;
							this.parent.search();
							this.parent.contentStyleChange();
						}
					});
				} else {
					this.$message.error(data.msg);
			   }
			});
		 }
         }
       });
    },
    // 获取uuid
    getUUID () {
      return new Date().getTime();
    },
    // 返回
    back() {
      this.parent.showFlag = true;
      this.parent.addOrUpdateFlag = false;
      this.parent.shiwuyingyangCrossAddOrUpdateFlag = false;
      this.parent.contentStyleChange();
    },
    shiwutupianUploadChange(fileUrls) {
	    this.ruleForm.shiwutupian = fileUrls;
    },
  }
};
</script>
<style lang="scss" scoped>
	.amap-wrapper {
		width: 100%;
		height: 500px;
	}
	
	.search-box {
		position: absolute;
	}
	
	.el-date-editor.el-input {
		width: auto;
	}
	
	.add-update-preview .el-form-item /deep/ .el-form-item__label {
	  	  padding: 0 10px 0 0;
	  	  color: #333;
	  	  font-weight: 600;
	  	  display: inline-block;
	  	  width: 180px;
	  	  font-size: inherit;
	  	  line-height: 40px;
	  	  text-align: right;
	  	}
	
	.add-update-preview .el-form-item /deep/ .el-form-item__content {
	  margin-left: 180px;
	}
	
	.add-update-preview .el-input /deep/ .el-input__inner {
	  	  padding: 0 12px;
	  	  color: inherit;
	  	  font-size: 14px;
	  	  border-color: #e1e8ee;
	  	  border-radius: 0px;
	  	  box-shadow: 0 0 0px rgba(64, 158, 255, .5);
	  	  outline: none;
	  	  background: #f5f8fa;
	  	  width: auto;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  min-width: 350px;
	  	  height: 32px;
	  	}
	.add-update-preview .el-input-number /deep/ .el-input__inner {
		text-align: left;
	  	  padding: 0 12px;
	  	  color: inherit;
	  	  font-size: 14px;
	  	  border-color: #e1e8ee;
	  	  border-radius: 0px;
	  	  box-shadow: 0 0 0px rgba(64, 158, 255, .5);
	  	  outline: none;
	  	  background: #f5f8fa;
	  	  width: auto;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  min-width: 350px;
	  	  height: 32px;
	  	}
	.add-update-preview .el-input-number /deep/ .el-input-number__decrease {
		display: none;
	}
	.add-update-preview .el-input-number /deep/ .el-input-number__increase {
		display: none;
	}
	
	.add-update-preview .el-select /deep/ .el-input__inner {
	  	  padding: 0 10px;
	  	  color: inherit;
	  	  font-size: 14px;
	  	  border-color: #e1e8ee;
	  	  border-radius: 0px;
	  	  box-shadow: 0 0 0px rgba(64, 158, 255, .5);
	  	  outline: none;
	  	  background: #f5f8fa;
	  	  width: auto;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  min-width: 350px;
	  	  height: 32px;
	  	}
	
	.add-update-preview .el-date-editor /deep/ .el-input__inner {
	  	  padding: 0 10px 0 30px;
	  	  color: inherit;
	  	  font-size: 14px;
	  	  border-color: #e1e8ee;
	  	  border-radius: 0px;
	  	  box-shadow: 0 0 0px rgba(64, 158, 255, .5);
	  	  outline: none;
	  	  background: #f5f8fa;
	  	  width: auto;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  min-width: 350px;
	  	  height: 32px;
	  	}
	
	.add-update-preview /deep/ .el-upload--picture-card {
		background: transparent;
		border: 0;
		border-radius: 0;
		width: auto;
		height: auto;
		line-height: initial;
		vertical-align: middle;
	}
	
	.add-update-preview /deep/ .upload .upload-img {
	  	  cursor: pointer;
	  	  color: #c0cfdc;
	  	  object-fit: cover;
	  	  font-size: 24px;
	  	  border-color: #e1e8ee;
	  	  line-height: 90px;
	  	  border-radius: 16px;
	  	  background: #f5f8fa;
	  	  width: 90px;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  text-align: center;
	  	  height: 90px;
	  	}
	
	.add-update-preview /deep/ .el-upload-list .el-upload-list__item {
	  	  cursor: pointer;
	  	  color: #c0cfdc;
	  	  object-fit: cover;
	  	  font-size: 24px;
	  	  border-color: #e1e8ee;
	  	  line-height: 90px;
	  	  border-radius: 16px;
	  	  background: #f5f8fa;
	  	  width: 90px;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  text-align: center;
	  	  height: 90px;
	  	}
	
	.add-update-preview /deep/ .el-upload .el-icon-plus {
	  	  cursor: pointer;
	  	  color: #c0cfdc;
	  	  object-fit: cover;
	  	  font-size: 24px;
	  	  border-color: #e1e8ee;
	  	  line-height: 90px;
	  	  border-radius: 16px;
	  	  background: #f5f8fa;
	  	  width: 90px;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  text-align: center;
	  	  height: 90px;
	  	}
	
	.add-update-preview .el-textarea /deep/ .el-textarea__inner {
	  	  padding: 12px;
	  	  color: inherit;
	  	  font-size: 14px;
	  	  border-color: #e1e8ee;
	  	  min-height: 120px;
	  	  border-radius: 0px;
	  	  box-shadow: 0 0 0px rgba(64, 158, 255, .5);
	  	  outline: none;
	  	  background: #f5f8fa;
	  	  width: auto;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  min-width: 550px;
	  	  height: auto;
	  	}
	
	.add-update-preview .btn .btn1 {
				border: 1px solid rgba(53, 184, 224, 0.1);
				cursor: pointer;
				padding: 0 10px;
				margin: 0px 4px;
				color: #fff;
				display: inline-block;
				font-size: 12px;
				line-height: 24px;
				border-radius: 2px;
				outline: none;
				background: #03a9f4;
				width: auto;
				height: 26px;
			}
	
	.add-update-preview .btn .btn1:hover {
				box-shadow: 0px 0px 9px #ccc;
				transform: translate3d(0px, 0px, 0px);
				opacity: 0.8;
			}
	
	.add-update-preview .btn .btn2 {
				border: 1px solid rgba(24, 138, 226, 0.1) ;
				cursor: pointer;
				border-radius: 2px;
				padding: 0 10px;
				margin: 0px 4px;
				outline: none;
				color: #fff;
				background: #6c757d;
				width: auto;
				font-size: 12px;
				line-height: 24px;
				height: 26px;
			}
	
	.add-update-preview .btn .btn2:hover {
				box-shadow: 0px 0px 9px #ccc;
				transform: translate3d(0px, 0px, 0px);
				opacity: 0.8;
			}
	
	.add-update-preview .btn .btn3 {
				border: 0px solid #0260ad;
				cursor: pointer;
				border-radius: 2px;
				padding: 0 20px;
				margin: 0px 4px;
				outline: none;
				color: #fff;
				background: #78bcee;
				width: auto;
				font-size: 12px;
				line-height: 24px;
				height: 26px;
			}
	
	.add-update-preview .btn .btn3:hover {
				box-shadow: 0px 0px 9px #ccc;
				transform: translate3d(0px, 0px, 0px);
				opacity: 0.8;
			}
	
	.add-update-preview .btn .btn4 {
				border: 0px solid rgba(126, 96, 16, .2);
				cursor: pointer;
				border-radius: 2px;
				padding: 0 20px;
				margin: 0px 4px;
				outline: none;
				color: #fff;
				background: #7dc855;
				width: auto;
				font-size: 12px;
				line-height: 24px;
				height: 26px;
			}
	
	.add-update-preview .btn .btn4:hover {
				box-shadow: 0px 0px 9px #ccc;
				transform: translate3d(0px, 0px, 0px);
				background: rgba(28,132,198,1);
				opacity: 1;
			}
	
	.add-update-preview .btn .btn5 {
				border: 0px solid rgba(114, 123, 132, 0.1);
				cursor: pointer;
				border-radius: 2px;
				padding: 0 20px;
				margin: 4px;
				outline: none;
				color: #fff;
				background: #fcce54;
				width: auto;
				font-size: 12px;
				line-height: 24px;
				height: 26px;
			}
	
	.add-update-preview .btn .btn5:hover {
				box-shadow: 0px 0px 9px #ccc;
				transform: translate3d(0px, 0px, 0px);
				opacity: 1;
			}
</style>

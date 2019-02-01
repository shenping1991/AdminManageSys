<template>
<div class="page-cash-list">
	<div class="cash-title">
		<span>回款</span>
	</div>
	<div class="cash-search">
		<span class="fs14 mr15">筛选:</span>
		<el-button type="primary" size="small" icon="search"></el-button>
		<el-button type="danger" size="small">重置</el-button>
	</div>
	<div class="cash-table">
	    <el-table :data="cashList" border style="width: 100%" highlight-current-row>
	    	<el-table-column label="流水号" width="180">
	            <template scope="scope">
	                <a href="javascript:;">{{scope.row.cashId}}</a>
	            </template>
	        </el-table-column>
	        <el-table-column label="回款编号" width="180">
	            <template scope="scope">
	                <a href="javascript:;">{{scope.row.ordId}}</a>
	            </template>
	        </el-table-column>
	       
	        <el-table-column label="回款金额" width="200">
	            <template scope="scope">
	                <span>{{ scope.row.cashAmount }}</span>
	            </template>
	        </el-table-column>
	        <el-table-column label="回款时间" width="200">
	            <template scope="scope">
	                <span>{{ scope.row.cashDate }}</span>
	            </template>
	        </el-table-column>
	        <el-table-column label="回款类型" width="200">
	            <template scope="scope">
	                <span>{{ scope.row.cashAccountType===0?"渠道回款":"直销回款" }}</span>
	            </template>
	        </el-table-column>
			 <el-table-column label="客户名称" width="200">
	            <template scope="scope">
	                <span>{{ scope.row.custoName }}</span>
	            </template>
	        </el-table-column>
	        <el-table-column label="负责人" width="200">
	            <template scope="scope">
	                <span>{{ scope.row.userName }}</span>
	            </template>
	        </el-table-column>
	    </el-table>
	</div>
</div>

</template>
<script>
	export default{
		data(){
			return{
				cashList:[
			    {
			        "cashId": "No20190101122334",
			        "ordId": "1",
			        "cashType": 0,
			        "payChannel": null,
			        "payType": null,
			        "cashStatus": 0,
			        "custoName": "上海测试有限公司",
			        "userName": "陈明",
			        "userDept": "华南渠道",
			        "cashAmount": 1222.56,
			        "cashDate": "2019-01-01",
			        "cashAccountType": 0,
			        "payNo": null
			    },
			    {
			        "cashId": "No20181212041245",
			        "ordId": "2",
			        "cashType": 0,
			        "payChannel": null,
			        "payType": null,
			        "cashStatus": 0,
			        "custoName": "山东测试有限公司",
			        "userName": "赵雷新",
			        "userDept": "华北渠道",
			        "cashAmount": 12332.00,
			        "cashDate": "2018-12-12",
			        "cashAccountType": 1,
			        "payNo": null
			    }]
			}
		}
	}
</script>
<style scope>
	.cash-title{
		padding: 15px;
		font-size: 20px;
	}
	.cash-search{
		padding: 10px 15px;
	}
</style>
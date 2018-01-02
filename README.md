# javaBasic
hello world

public static RbBalanceQueryService getDubboService(){
		try {
			if(balanceQueryService==null)
				balanceQueryService = DubboServiceLoader.getInstance().getReferedService("balanceQuery_rb");
			BizLogger.info("BankCardProxy.initService", "BankCardProxy init rbBindCardService");
		} catch (Throwable th) {
			BizLogger.error(th, "BankCardProxy init rbBindCardService error~~");
			balanceQueryService = DubboServiceLoader.getInstance().getReferedService("balanceQuery_rb");
		}
		return balanceQueryService;
	}

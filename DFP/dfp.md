# DFP querry 
DFP querry for fetching order Data by order id 
        OrderPage orderPage = orderService.getOrdersByStatement(new StatementBuilder().where("id IN (" +your order id +")").toStatement());
for multiple orders pass orderids as `id1,id2,id3,.,.` pass by `,` seperated values.
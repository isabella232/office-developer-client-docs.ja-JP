---
title: project Online でユーザー設定フィールドを一括更新し、プロジェクトサイトを作成する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: お客様が project online を最大限に活用し、サービスの拡張性と柔軟性を向上させるために、project online のアプリとワークフローで使用できるクライアント側オブジェクトモデルに2つのメソッドを追加しました。
ms.openlocfilehash: 4de42471cd8c2f12a982447ccffc27ec8104fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355401"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Project Online でユーザー設定フィールドを一括更新し、ワークフローからプロジェクト サイトを作成する

お客様が project online を最大限に活用し、サービスの拡張性と柔軟性を向上させるために、project online のアプリとワークフローで使用できるクライアント側オブジェクトモデルに2つのメソッドを追加しました。
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |プロジェクトユーザー設定フィールドを一括更新します。 Project Online の場合のみ。 REST API でのみ使用できます。  <br/> |
|**CreateProjectSite** <br/> | プロジェクトサイトを作成します。 Project Online の場合のみ。 REST API、マネージクライアントオブジェクトモデル、および JavaScript クライアントオブジェクトモデルで使用できます。  <br/> |
   
これらの方法では、柔軟性が向上するだけでなく、プロジェクトをワークフローに保存して発行するときのパフォーマンスも大幅に向上しています。 この記事では、REST API のメソッドを使用する方法について説明し、ユーザー設定フィールドおよびプロジェクトサイトを作成するワークフローを一括で更新するワークフローを作成するための手順を示します。
  
> [!NOTE]
> sharepoint 2013 ワークフローから REST api を呼び出す方法の詳細については、「 [POST メソッドを使用してワークフローから sharepoint rest サービスを使用](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl)する」および「sharepoint [Designer ワークフローから sharepoint 2013 rest api を呼び出す](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/)」を参照してください。 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>ワークフローからのプロジェクトユーザー設定フィールドの一括更新
<a name="BulkUpdateCustomFields"> </a>

以前は、ワークフローは一度に1つのユーザー設定フィールドしか更新できませんでした。 一度に1つのプロジェクトユーザー設定フィールドを更新すると、ユーザーがプロジェクト詳細ページ間を移行するときに、エンドユーザーの作業が遅くなる可能性があります。 各更新プログラムでは、[**プロジェクトフィールドの設定]** アクションを使用して、複数のユーザー設定フィールドを高待機時間の低帯域幅のネットワーク上で更新することによって、単純なオーバーヘッドが発生しました。 この問題を解決するには、 **UpdateCustomFields**メソッドを REST API に追加して、ユーザー設定フィールドを一括更新できるようにしました。 **UpdateCustomFields**を使用するには、更新するすべてのユーザー設定フィールドの名前と値を含むディクショナリを渡します。
  
REST メソッドは、次のエンドポイントにあります。
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> 例の`<site-url>`プレースホルダーを、project Web App (PWA) サイトの URL、およびプロジェクト UID を含む`<guid>`プレースホルダーに置き換えます。 
  
このセクションでは、プロジェクトのユーザー設定フィールドを一括更新するワークフローを作成する方法について説明します。 ワークフローは、次の大まかな手順に従います。
  
- 更新するプロジェクトがチェックインされるまで待機する
    
- プロジェクトのすべてのユーザー設定フィールドの更新を定義するデータセットを構築する
    
- プロジェクトをチェックアウトする
    
- **UpdateCustomFields**を呼び出して、ユーザー設定フィールドの更新をプロジェクトに適用します。 
    
- 関連情報をワークフロー履歴リストに記録する (必要な場合)
    
- プロジェクトを発行する
    
- プロジェクトをチェックインする
    
最終的なエンドツーエンドのワークフローは、次のようになります。
  
![エンドツーエンドのワークフロー](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "エンドツーエンドのワークフロー")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>ユーザー設定フィールドを一括更新するワークフローを作成するには

1. 省略可能です。 ワークフロー全体で使用できる変数に、プロジェクトの完全な URL を格納します。
    
    ![プロジェクトの URL を変数に格納する](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "プロジェクトの URL を変数に格納する")
  
2. [**プロジェクトイベントの待機**] アクションをワークフローに追加し、[**プロジェクトのチェックイン時**] イベントを選択します。 
    
    ![プロジェクトがチェックインされるまで待機する](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "プロジェクトがチェックインされるまで待機する")
  
3. 「Create **dictionary** action」アクションを使用して、 **requestHeader**辞書を作成します。 このワークフローのすべての web サービス呼び出しに対して同じ要求ヘッダーを使用します。 
    
    ![requestHeader 辞書を作成する](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "requestHeader 辞書を作成する")
  
4. 次の2つの項目をディクショナリに追加します。
    
    |名前|型|値|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |application/json;odata = verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |application/json;odata = verbose  <br/> |
   
    ![Accept ヘッダーの追加](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept ヘッダーの追加")
  
5. 「**辞書を構築**する」アクションを使用して、 **requestbody**辞書を作成します。 この辞書には、適用するすべてのフィールドの更新が格納されます。 
    
    各ユーザー設定フィールドの更新では、フィールドの (1) メタデータ型、(2) キー、(3) 値、および (4) 値の型の4つの行が必要です。
    
    - **__ メタデータ/型**フィールドのメタデータ型。 このレコードは常に同じであり、次の値を使用します。 
    
       - Name: customfielddictionary (i)/__ metadata/type (ここで、 **i**は0から始まる辞書内の各ユーザー設定フィールドのインデックス) 
            
       - 型:String
            
       - 値: SP。KeyValue
    
       ![ユーザー設定フィールドの更新を定義する](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "ユーザー設定フィールドの更新を定義する")
  
    - **キー**ユーザー設定フィールドの内部名 (形式: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       **InternalName**エンドポイントに移動することで、ユーザー設定フィールドの内部名を検索できます。`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       ユーザー設定フィールドを手動で作成した場合、値はサイトごとに異なります。 複数のサイト間でワークフローを再利用することを計画している場合は、ユーザー設定フィールド id が正しいことを確認してください。
    
    - **値**ユーザー設定フィールドに割り当てる値を指定します。 参照テーブルにリンクされているユーザー設定フィールドの場合は、実際の参照テーブルの値の代わりに、参照テーブルのエントリの内部名を使用する必要があります。 
    
       参照テーブルエントリの内部名は、次のエンドポイントで確認できます。`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       複数の値を受け入れるように参照テーブルのユーザー設定フィールドが設定さ`;#`れている場合は、を使用して値を連結します (下記の辞書例を参照)。 
    
    - **ValueType**更新するユーザー設定フィールドの種類を示します。 
    
       - Text、Duration、Flag、および lookuptable フィールドの場合は、Edm を使用します。
    
       - 数値フィールドの場合は、edm を使用して、またはその他の OData 承認番号の種類を使用します。
    
       - 日付フィールドについては、Edm を使用します。
    
       次の辞書例では、3つのユーザー設定フィールドの更新を定義しています。 1つ目は、複数値の参照テーブルのユーザー設定フィールドで、2番目は数値フィールドで、3番目は日付フィールド用です。 **customfielddictionary**インデックスがどのようにインクリメントされるかに注目してください。 
    
       > [!NOTE]
       > これらの値は、説明のみを目的としています。 使用するキーと値のペアは、PWA のデータによって異なります。 
  
       |名前|型|値|
       |:-----|:-----|:-----|
       |customfielddictionary (0)/__ metadata/type  <br/> |String  <br/> |sp2.KeyValue  <br/> |
       |customfielddictionary (0)/キー  <br/> |String  <br/> |カスタム\_ce23fbf43fa0e411941000155d3c8201  <br/> |
       |customfielddictionary (0)/Value  <br/> |String  <br/> |Entry\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201  <br/> |
       |customfielddictionary (0)/ValueType  <br/> |String  <br/> |Edm.String  <br/> |
       |customfielddictionary (1)/__ metadata/type  <br/> |String  <br/> |sp2.KeyValue  <br/> |
       |customfielddictionary (1)/キー  <br/> |String  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customfielddictionary (1)/Value  <br/> |String  <br/> |90.5  <br/> |
       |customfielddictionary (1)/ValueType  <br/> |String  <br/> |Edm.Double  <br/> |
       |customfielddictionary (2)/__ metadata/type  <br/> |String  <br/> |sp2.KeyValue  <br/> |
       |customfielddictionary (2)/キー  <br/> |String  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customfielddictionary (2)/Value  <br/> |String  <br/> |2015-04-01t00:00: 00.0000000  <br/> |
       |customfielddictionary (2)/ValueType  <br/> |String  <br/> |Edm.DateTime  <br/> |
   
       ![ユーザー設定フィールドの更新を定義する辞書](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "ユーザー設定フィールドの更新を定義する辞書")
  
6. [ **HTTP Web サービスの呼び出し**] アクションを追加して、プロジェクトをチェックアウトします。 
    
    ![Checkout メソッドを呼び出す](media/8ce56014-0317-419b-afa7-229d05c86885.png "Checkout メソッドを呼び出す")
  
7. web サービス呼び出しのプロパティを編集して、要求ヘッダーを指定します。 [**プロパティ**] ダイアログボックスを開くには、アクションを右クリックして [**プロパティ**] を選択します。
    
    ![web サービス呼び出しプロパティで要求ヘッダーを指定する](media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "web サービス呼び出しプロパティで要求ヘッダーを指定する")
  
8. **UpdateCustomFields**メソッドを呼び出す**HTTP Web サービスの呼び出し**アクションを追加します。 
    
    ![HTTP Web サービスの呼び出しアクションを作成する](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "HTTP Web サービスの呼び出しアクションを作成する")
  
    web サービス`/Draft/` URL のセグメントをメモします。 完全な URL は次のようになります。`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![UpdateCustomFields メソッドを呼び出す](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "UpdateCustomFields メソッドを呼び出す")
  
9. web サービス呼び出しのプロパティを編集して、作成した辞書に**RequestHeader**および**requestcontent**パラメーターをバインドします。 また、新しい変数を作成して、応答可能な**テント**を格納することもできます。
    
    ![要求ヘッダーとコンテンツに辞書をバインドする](media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "要求ヘッダーとコンテンツに辞書をバインドする")
  
10. 省略可能です。 応答ディクショナリから読み取り、キュージョブの状態を確認し、ワークフロー履歴リストに情報を記録します。
    
    ![ログの設定](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "ログの設定")
  
11. web サービス呼び出しを**発行**エンドポイントに追加して、プロジェクトを発行します。 常に同じ要求ヘッダーを使用します。 
    
    ![Publish メソッドを呼び出す](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Publish メソッドを呼び出す")
  
    ![発行 web サービスの呼び出しのプロパティ](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "発行 web サービスの呼び出しのプロパティ")
  
12. プロジェクトをチェックインするための、最後の web サービス呼び出しを**Checkin**エンドポイントに追加します。 
    
    ![Checkin メソッドを呼び出す](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Checkin メソッドを呼び出す")
  
    ![Checkin web サービス呼び出しのプロパティ](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "Checkin web サービス呼び出しのプロパティ")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>ワークフローからプロジェクトサイトを作成する

各プロジェクトには、チームメンバーが共同作業を行ったり、ドキュメントを共有したり、問題を発生させたりできる、独自の専用の SharePoint サイトを含めることができます。 以前は、サイトは、最初に発行するとき、または project Professional のプロジェクトマネージャー、または管理者が PWA 設定で手動で作成することができます。または、無効にすることもできます。
  
プロジェクトサイトを作成するタイミングを選択できるように、 **createprojectsite**メソッドを追加しました。 これは、プロジェクト提案が最初の発行時ではなく、定義済みのワークフローの特定のステージに達したときに、サイトを自動的に作成する必要がある組織に特に便利です。 プロジェクトサイトの作成を延期すると、プロジェクトの作成のパフォーマンスが大幅に向上します。 
  
**前提条件:****createprojectsite**を使用できるようにするには、「 **PWA**設定 > * * 接続された SharePoint サイト * * > の**設定**で、 **[ユーザーに選択を許可する]** 設定を [プロジェクトサイトの作成] に設定する必要があります。
  
![PWA 設定で [ユーザーに選択を許可する]] を設定する(media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "ユーザーが PWA 設定で選択できるようにする設定")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>プロジェクトサイトを作成するワークフローを作成するには

1. 既存のワークフローを作成または編集し、プロジェクトサイトを作成する手順を選択します。
    
2. 「Create **dictionary** action」アクションを使用して、 **requestHeader**辞書を作成します。 
    
    ![requestHeader 辞書を作成する](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "requestHeader 辞書を作成する")
  
3. 次の2つの項目をディクショナリに追加します。
    
    |名前|型|値|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |application/json;odata = verbose  <br/> |
    |Content-Type  <br/> |String  <br/> |application/json;odata = verbose  <br/> |
   
    ![Accept ヘッダーの追加](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept ヘッダーの追加")
  
4. [ **HTTP Web サービスの呼び出し**] アクションを追加します。 **POST**を使用するように要求の種類を変更し、次の形式を使用して URL を設定します。
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![createprojectsite エンドポイント URI を作成する](media/42a90a5e-8d1b-4667-a933-785175212847.png "createprojectsite エンドポイント URI を作成する")
  
    プロジェクトサイトの名前を文字列として**createprojectsite**メソッドに渡します。 プロジェクト名をサイト名として使用するには、空の文字列を渡します。 次に作成するプロジェクトサイトが機能するように、一意の名前を使用してください。 
    
5. web サービス呼び出しのプロパティを編集して、作成した辞書に**RequestHeader**パラメーターをバインドします。 
    
    ![要求への辞書のバインド](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "要求への辞書のバインド")
  
## <a name="see-also"></a>関連項目

- [Project のプログラミング タスク](project-programming-tasks.md)
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)
- [SharePoint 2013 のワークフロー](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    


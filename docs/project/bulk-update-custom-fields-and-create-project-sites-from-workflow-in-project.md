---
title: ユーザー設定フィールドの更新プログラムを一括して、オンラインのプロジェクトにプロジェクト サイトを作成
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 815131c6-190c-4f29-83bf-c853eee72821
description: お客様のオンライン プロジェクトを最大限に活用し、当社のサービスの拡張性と柔軟性を向上させるために、2 つの方法オンライン プロジェクトのアプリケーションとワークフローで使用できるクライアント側オブジェクト モデルに追加しました。
ms.openlocfilehash: 4de42471cd8c2f12a982447ccffc27ec8104fa31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386160"
---
# <a name="bulk-update-custom-fields-and-create-project-sites-from-a-workflow-in-project-online"></a>Project Online でユーザー設定フィールドを一括更新し、ワークフローからプロジェクト サイトを作成する

お客様のオンライン プロジェクトを最大限に活用し、当社のサービスの拡張性と柔軟性を向上させるために、2 つの方法オンライン プロジェクトのアプリケーションとワークフローで使用できるクライアント側オブジェクト モデルに追加しました。
  
|||
|:-----|:-----|
|**UpdateCustomFields** <br/> |一括では、プロジェクトのユーザー設定フィールドを更新します。 オンライン プロジェクトのみです。 REST API でのみ使用できます。  <br/> |
|**CreateProjectSite** <br/> | プロジェクト サイトを作成します。 オンライン プロジェクトのみです。 REST API、マネージ クライアント オブジェクト モデル、および JavaScript クライアント オブジェクト モデルで使用できます。  <br/> |
   
高い柔軟性を提供し、これらのメソッドは、保存とワークフロー内でプロジェクトを発行するときに、大幅なパフォーマンス向上も提供します。 ここでは、REST API のメソッドを使用する方法について説明し、その一括更新のユーザー設定フィールドおよびプロジェクトのサイトを作成するワークフローは、ワークフローを作成する方法について説明します。
  
> [!NOTE]
> SharePoint 2013 ワークフローから REST Api を呼び出す方法の詳細については、 [POST メソッドを使用してワークフローからを使用して SharePoint の他のサービス](https://mysharepointinsight.blogspot.com/2013/05/using-sharepoint-rest-services-from.mdl)と[SharePoint ワークフロー デザイナーから SharePoint 2013 の Rest API の呼び出し](https://sergeluca.wordpress.com/2013/04/09/calling-the-sharepoint-2013-rest-api-from-a-sharepoint-designer-workflow/)を参照してください。 
  
## <a name="bulk-update-project-custom-fields-from-a-workflow"></a>ワークフローの一括更新プロジェクトのユーザー設定フィールド
<a name="BulkUpdateCustomFields"> </a>

以前は、ワークフローは一度に 1 つのユーザー設定フィールドを更新する可能性がありますだけです。 1 つのプロジェクト ユーザー設定フィールドを更新する場合は、プロジェクト詳細ページ間でユーザーの移行とに不適切なエンド ユーザー エクスペリエンスを可能性があります。 各更新プログラムには、**プロジェクト フィールドの設定**アクションを使用して別のサーバー要求が必要な高レーテンシーの複数のユーザー設定フィールドを更新するには、低帯域幅ネットワークの結果、重要なオーバーヘッドです。 この問題を解決するには、REST API を一括することがユーザー設定フィールドを更新する**UpdateCustomFields**メソッドを追加しました。 **UpdateCustomFields**を使用するには、名前と、更新するすべてのユーザー設定フィールドの値を格納しているディクショナリを渡します。
  
残りの部分メソッドに次の端点にあります。
  
`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
  
> [!NOTE]
> 交換して、 `<site-url>` 、Project Web App (PWA) サイトの URL の例ではプレース ホルダーと、 `<guid>` 、プロジェクトの UID を持つプレース ホルダー。 
  
このセクションでは、プロジェクトのユーザー設定フィールドを一括で更新するワークフローを作成する方法について説明します。 ワークフローは、これらの大まかな手順を次に示します。
  
- プロジェクト チェック アウトを取得するのにを更新するまで待つ
    
- プロジェクト用に、ユーザー設定フィールドのすべての更新を定義するデータ セットを作成します。
    
- プロジェクトをチェック アウト
    
- プロジェクトにユーザー設定フィールドの更新プログラムを適用する**UpdateCustomFields**を呼び出す 
    
- (必要な場合)、ワークフロー履歴リストに関連する情報をログに記録します。
    
- プロジェクトを発行する
    
- プロジェクトをチェックインします。
    
最後に、エンド ・ ツー ・ エンドのワークフローは、次のようになります。
  
![エンド ・ ツー ・ エンドのワークフロー](media/8c0741f9-7f76-409d-8c00-e7a8c3ddb89f.png "エンド ・ ツー ・ エンドのワークフロー")
  
### <a name="to-create-a-workflow-that-bulk-updates-custom-fields"></a>一括でユーザー設定フィールドを更新するワークフローを作成するには

1. 省略可能。 ワークフロー全体で使用できる変数には、プロジェクトの完全な URL を格納します。
    
    ![ストア変数内のプロジェクトの URL](media/a880c5c6-8e7a-44dd-87e9-7e532169d489.png "ストア変数内のプロジェクトの URL")
  
2. **プロジェクト イベントを待機**アクションをワークフローに追加し、**プロジェクトをチェックインするとき**のイベントを選択します。 
    
    ![プロジェクトをチェックインするまで待ちます](media/699aa9c7-b3c9-426e-a775-96993a13559c.png "プロジェクトをチェックインするまで待ちます")
  
3. **ディクショナリのビルド**アクションを使用して**requestHeader**辞書を作成します。 このワークフローで web サービスを呼び出すすべての同一の要求ヘッダーを使用します。 
    
    ![RequestHeader ディクショナリを構築します。](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "RequestHeader ディクショナリを構築します。")
  
4. 辞書には、次の 2 つの項目を追加します。
    
    |名前|種類|値|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |アプリケーションまたは json です。odata = 詳細  <br/> |
    |Content-Type  <br/> |String  <br/> |アプリケーションまたは json です。odata = 詳細  <br/> |
   
    ![Accept ヘッダーを追加します。](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept ヘッダーを追加します。")
  
5. **ディクショナリのビルド**アクションを使用して**requestBody**辞書を作成します。 このディクショナリでは、適用するすべてのフィールドの更新を格納します。 
    
    各ユーザー設定フィールドの更新プログラムには、4 つの行が必要です: フィールドのメタデータ (1) 型、キー (2)、(3) の値、および (4) の値型です。
    
    - **__metadata/タイプ**フィールドのメタデータのタイプです。 このレコードは、常に同じと次の値を使用しています。 
    
       - 名: customFieldDictionary (i)/__metadata/タイプ ( **i**は 0 から始まる、ディクショナリ内の各ユーザー設定フィールドのインデックス) 
            
       - 型:String
            
       - 値: sp へKeyValue
    
       ![ユーザー設定フィールドの更新プログラムを定義します。](media/a4423493-6603-42ee-ae50-1ef74c5c59bd.png "ユーザー設定フィールドの更新プログラムを定義します。")
  
    - **キー**形式で、ユーザー設定フィールドの内部名: *Custom_ce23fbf43fa0e411941000155d3c8201* 
    
       **InternalName**エンドポイントに移動すると、ユーザー設定フィールドの内部名をご覧ください。`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/InternalName`
    
       ユーザー設定フィールドを手動で作成した場合の値をサイトからサイトへと異なります。 複数のサイト間でワークフローを再利用する場合は、ユーザー設定フィールド Id が正しいことを確認します。
    
    - **値**ユーザー設定フィールドに割り当てる値です。 ルックアップ テーブルにリンクされているユーザー設定フィールド、実際の参照テーブルの値の代わりにルックアップ テーブルのエントリの内部名を使用する必要があります。 
    
       次のエンドポイントでは内部参照テーブルのエントリの名前をご覧ください。`https://<site-url>/_api/ProjectServer/CustomFields('<guid>')/LookupEntries('<guid>')/InternalName`
    
       ルックアップ テーブル カスタム フィールド セットに複数の値をそのまま使用、使用した場合`;#`に示すように次の例の辞書) の値を連結します。 
    
    - **値型**更新するにはユーザー設定フィールドの型。 
    
       - テキスト、期間、フラグ、および LookupTable のフィールドの Edm.String を使用して、
    
       - 数値フィールドは、「Edm.Int32、Edm.Double、またはその他の OData に受け入れられている数値型の使用」を使用していますください。
    
       - 日付フィールドでは、Edm.DateTime を使用して、
    
       下の辞書の例では、次の 3 つのユーザー設定フィールド用の更新プログラムを定義します。 複数値ルックアップ テーブルのカスタム フィールドは、最初、2 番目の数値型フィールドでは、日付フィールドには、3 つ目。 注方法**customFieldDictionary**インデックスの増分値です。 
    
       > [!NOTE]
       > これらの値は、例示目的でのみです。 使用するキーと値のペアは、PWA のデータによって異なります。 
  
       |名前|種類|値|
       |:-----|:-----|:-----|
       |customFieldDictionary (0)/__metadata/タイプ  <br/> |String  <br/> |SP へKeyValue  <br/> |
       |customFieldDictionary (0)/キー  <br/> |String  <br/> |カスタム\_ce23fbf43fa0e411941000155d3c8201  <br/> |
       |customFieldDictionary (0)/値  <br/> |String  <br/> |エントリ\_b9a2fd69279de411940f00155d3c8201; #Entry\_baa2fd69279de411940f00155d3c8201  <br/> |
       |customFieldDictionary (0) または値型  <br/> |String  <br/> |Edm.String  <br/> |
       |customFieldDictionary (1)/__metadata/タイプ  <br/> |String  <br/> |SP へKeyValue  <br/> |
       |customFieldDictionary (1)/キー  <br/> |String  <br/> |Custom_c7f114c97098e411940f00155d3c8201  <br/> |
       |customFieldDictionary (1) と値  <br/> |String  <br/> |90.5  <br/> |
       |customFieldDictionary (1) または値型  <br/> |String  <br/> |Edm.Double  <br/> |
       |customFieldDictionary (2)/__metadata/タイプ  <br/> |String  <br/> |SP へKeyValue  <br/> |
       |customFieldDictionary (2)/キー  <br/> |String  <br/> |Custom_c6fb67e0b9a1e411941000155d3c8201  <br/> |
       |customFieldDictionary (2) と値  <br/> |String  <br/> |2015-04-01T00:00:00.0000000  <br/> |
       |customFieldDictionary (2) または値型  <br/> |String  <br/> |Edm.DateTime  <br/> |
   
       ![辞書の更新プログラムのユーザー設定フィールドを定義します。](media/41a1f18f-a6b2-40ff-904b-437baf962621.png "辞書の更新プログラムのユーザー設定フィールドを定義します。")
  
6. プロジェクトをチェック アウトするには、 **HTTP Web サービスを呼び出す**アクションを追加します。 
    
    ![Checkout メソッドを呼び出す](media/8ce56014-0317-419b-afa7-229d05c86885.png "Checkout メソッドを呼び出す")
  
7. Web サービス呼び出しの要求ヘッダーを指定するのプロパティを編集します。 **プロパティ**] ダイアログ ボックスを開くには、アクションを右クリックして**プロパティ**を選択します。
    
    ![プロパティを呼び出す web サービスの要求ヘッダーの指定](media/d81e92b1-43df-42ad-9cd0-a693f93b164e.png "プロパティを呼び出す web サービスの要求ヘッダーの指定")
  
8. **UpdateCustomFields**メソッドを呼び出して、 **HTTP Web サービスを呼び出す**アクションを追加します。 
    
    ![HTTP Web サービスを呼び出すアクションを作成します。](media/9a73a201-c035-41b4-8798-506ac48b90f8.png "HTTP Web サービスを呼び出すアクションを作成します。")
  
    注、 `/Draft/` 、web サービスの URL のセグメントです。 完全な URL は、次のようになります。`https://<site-url>/_api/ProjectServer/Projects('<guid>')/Draft/UpdateCustomFields()`
    
    ![UpdateCustomFields メソッドを呼び出す](media/03b323f1-8e99-4b18-be18-be505d7cec7e.png "UpdateCustomFields メソッドを呼び出す")
  
9. 作成した辞書を**RequestHeader**と**RequestContent**のパラメーターをバインドする web サービスの呼び出しのプロパティを編集します。 **ResponseContent**を格納する新しい変数を作成することもできます。
    
    ![要求ヘッダーとコンテンツの辞書をバインドします。](media/f96bec92-138e-4eab-b1e7-1ab83d0428a5.png "要求ヘッダーとコンテンツの辞書をバインドします。")
  
10. 省略可能。 キュー ジョブの状態を確認し、ワークフローの履歴リストに情報をログに記録する応答のディクショナリから読み込まれます。
    
    ![ログの設定](media/7d2f4936-61d7-4906-83e8-7478a5935af5.png "ログの設定")
  
11. プロジェクトを発行する**発行**エンドポイントに web サービスの呼び出しを追加します。 常に同じ要求ヘッダーを使用します。 
    
    ![Publish メソッドを呼び出す](media/3b661091-ffae-4d7e-a0bb-5b96a6292731.png "Publish メソッドを呼び出す")
  
    ![発行 web サービスのプロパティを呼び出す](media/6a80a5d3-7e29-4398-993c-f78b3faca8b1.png "発行 web サービスのプロパティを呼び出す")
  
12. プロジェクトをチェックインする**チェックイン**のエンドポイントに最終的な web サービス呼び出しを追加します。 
    
    ![Checkin メソッドを呼び出す](media/430510cb-0774-4911-af7f-b565b83eba0e.png "Checkin メソッドを呼び出す")
  
    ![チェックイン web サービスのプロパティを呼び出す](media/485f48d6-bbb8-4568-9dc3-aae3218f6bd1.png "チェックイン web サービスのプロパティを呼び出す")

<a name="CreateProjectSite"> </a>

## <a name="create-a-project-site-from-a-workflow"></a>ワークフローからのプロジェクト サイトを作成します。

すべてのプロジェクトは、チーム メンバーが共同作業を行うドキュメントを共有、問題を発生させるに表示され、それぞれ専用の SharePoint サイトを持つことができます。 以前は、サイトがのみを作成する自動的に発行または手動で Project Professional でプロジェクト マネージャーまたは管理者は、PWA での設定、またはそれらを無効にでした。
  
プロジェクト サイトを作成する場合に選択することができますので、 **CreateProjectSite**メソッドを追加しました。 これは、組織ユーザーが最初に発行するのではなく、プロジェクトの提案が、定義済みのワークフローの特定の段階に達すると自動的に自分のサイトを作成する場合に特に役立ちます。 プロジェクト サイトの作成を大幅に延期すると、プロジェクトの作成のパフォーマンスが向上します。 
  
**前提条件:****PWA の設定**でプロジェクト サイトの作成**を選択するユーザーを許可する**設定を設定する必要があります**CreateProjectSite**を使用する前に > * * 接続されている SharePoint サイト * * >**設定**します。
  
![の設定「を許可するユーザーを選択する」PWA の設定で](media/6c6c8175-eb10-431d-8056-cea55718fdb4.png "PWA の設定を選択する設定が可能にします。")
  
### <a name="to-create-a-workflow-that-creates-a-project-site"></a>プロジェクト サイトを作成するワークフローを作成するには

1. 作成または既存のワークフローを編集し、プロジェクト サイトを作成するステップを選択します。
    
2. **ディクショナリのビルド**アクションを使用して**requestHeader**辞書を作成します。 
    
    ![RequestHeader ディクショナリを構築します。](media/83b0aa10-9ab7-43dd-800d-a738bb815876.png "RequestHeader ディクショナリを構築します。")
  
3. 辞書には、次の 2 つの項目を追加します。
    
    |名前|種類|値|
    |:-----|:-----|:-----|
    |Accept  <br/> |String  <br/> |アプリケーションまたは json です。odata = 詳細  <br/> |
    |Content-Type  <br/> |String  <br/> |アプリケーションまたは json です。odata = 詳細  <br/> |
   
    ![Accept ヘッダーを追加します。](media/2f2e2016-3c49-4cac-b1e7-f2b8118b840c.png "Accept ヘッダーを追加します。")
  
4. **HTTP Web サービスを呼び出す**アクションを追加します。 **POST**を使用する要求の種類を変更し、次の形式を使用して URL を設定します。
    
    `https://<site-url>/_api/ProjectServer/Projects('<guid>')/CreateProjectSite('New web name')`
    
    ![CreateProjectSite エンドポイントの URI を構築します。](media/42a90a5e-8d1b-4667-a933-785175212847.png "CreateProjectSite エンドポイントの URI を構築します。")
  
    プロジェクト サイトの名前を**CreateProjectSite**メソッドに文字列として渡します。 サイト名としてプロジェクト名を使用するには、空の文字列を渡します。 作業は、次にプロジェクト サイトを作成するために一意の名前を使用することを確認します。 
    
5. 作成した辞書を**RequestHeader**パラメーターにバインドする web サービスの呼び出しのプロパティを編集します。 
    
    ![要求する辞書をバインド](media/61a5a0a8-405f-44eb-b5e7-80b11f7caec3.png "要求する辞書をバインド")
  
## <a name="see-also"></a>関連項目

- [Project のプログラミング タスク](project-programming-tasks.md)
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)
- [Microsoft SharePoint 2010 SDK へようこそ](https://msdn.microsoft.com/library/e0602371-ae22-44be-8a7e-9e47e9f046d6%28Office.15%29.aspx)
    


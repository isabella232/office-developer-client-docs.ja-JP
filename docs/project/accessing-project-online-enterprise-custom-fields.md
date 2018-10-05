---
title: Project Online エンタープライズ ユーザー設定フィールドへのアクセス
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: オンラインのプロジェクトは、企業はビジネス ニーズに合わせて拡張可能な Office 365 サービスです。 1 つの拡張領域は、エンタープライズ ユーザー設定フィールド (ECFs) です。 ECFs は、プロジェクト、リソース、およびタスクに追加できる型指定された値フィールドです。 次の表では、プロジェクト、リソース、およびタスクに関連する ECFs を一覧表示し、その ECF のインスタンスの値の例が用意されています。
ms.openlocfilehash: 978fdfbf4ba75382ad85b9f92f8ac4df5c7f97c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401154"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a>Project Online エンタープライズ ユーザー設定フィールドへのアクセス

オンラインのプロジェクトは、企業はビジネス ニーズに合わせて拡張可能な Office 365 サービスです。 1 つの拡張領域は、エンタープライズ ユーザー設定フィールド (ECFs) です。 ECFs は、プロジェクト、リソース、およびタスクに追加できる型指定された値フィールドです。 次の表では、プロジェクト、リソース、およびタスクに関連する ECFs を一覧表示し、その ECF のインスタンスの値の例が用意されています。
  
|ECF 名|ECF の種類|Association|例の値|
|:-----|:-----|:-----|:-----|
|妥当性  <br/> |TEXT  <br/> |Project  <br/> |エンド ・ ユーザーは、重要な統計のデータと状態データ、正常性評価と個別化されたアクションを含む検索結果を記録できる良好な状態の方に計画します。  <br/> |
|リスクの評価  <br/> |TEXT  <br/> |Project  <br/> |低  <br/> |
|ROI  <br/> |番号  <br/> |Project  <br/> |2.10  <br/> |
|総所有コスト  <br/> |コスト  <br/> |Project  <br/> |1,031,514 ドル  <br/> |
|チームを起動します。  <br/> |TEXT  <br/> |Resources  <br/> |はい  <br/> |
|位置の役割  <br/> |TEXT  <br/> |リソース  <br/> |テスト担当者  <br/> |
|フラグ  <br/> |フラグ  <br/> |タスク  <br/> |いいえ  <br/> |
|タスクの状況  <br/> |TEXT  <br/> |タスク  <br/> |指定されていません  <br/> |
   
ECFs は、プロジェクト Web アプリケーション (PWA) インスタンスでは、任意のプロジェクト、リソース、またはタスクから外部で定義されます。 まだ、プロジェクト、リソース、またはタスクに関連付けられていることになります。 この資料では、サンプル アプリケーションを使用してユーザー設定のフィールドに必須の外観を提供し、ECF の値を取得するのに焦点を当てます。 
  
完全なサンプルをダウンロードすることができますhttps://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields。
  
さらに、オンラインのプロジェクトをサポートしているローカル ユーザー設定フィールド、特定のプロジェクト、リソース、またはタスクに固有のエンティティを読み取り専用として。 ローカル ユーザー設定フィールドの詳細については、サンプルを参照してくださいhttps://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\。
  
## <a name="background-materials"></a>背景資料

[クライアント側オブジェクト モデルを使用してプロジェクトのオンライン アプリケーションの開発](developing-a-project-online-application-using-the-client-side-object-model.md)を、前回の記事では、バック グラウンドと CSOM を使用してアプリケーションを開発するための最初の方向を提供します。 次の項目は、この資料を参照してください。
  
- プロジェクト、およびクラウド ベースのスタンドアロン版についての基礎知識 
    
- 開発環境 (Visual Studio のエディションおよびソフトウェア ライブラリ)
    
- CSOM ライブラリを使用して .NET アプリケーション用の Visual Studio のプロジェクトの設定
    
- プロジェクトのオンライン サービスに接続します。
    
## <a name="preliminaries-class-level-declarations"></a>準備 (クラス レベルの宣言)

このアプリケーションのクラスは、2 つのデータ項目を定義します。 プロジェクト コンテキストと pwaECF の辞書です。
  
プロジェクト コンテキスト オブジェクトはプロジェクト CSOM の一部であるため、アプリケーション、PWA のインスタンスに接続します。 サービスに対するすべての要求は、プロジェクトのコンテキストを使用します。
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

コンテキストには、接続のエンドポイントをアプリケーションでインスタンスを作成する必要があります。 接続のエンドポイントは、PWA インスタンスの URL です。 
  
PwaECF ディクショナリには、ECFs は、PWA のレベルで定義されているプロジェクトが格納されています。 ディクショナリは、ECF を使用します。キーと値としてのカスタム オブジェクトとして InternalName。 辞書は、ListPWACustomFields メソッドで作成され、Main メソッド内の参照として使用されます。 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a>Main メソッド

Main メソッドは、アプリケーションのフローを管理します。 として、プロジェクトのオンライン CSOM を使用する他のアプリケーションのメイン コンテキストを初期化プロジェクトです。 
  
1. 取得し、プロジェクトのオンライン PWA で ECFs を一覧表示します。
    
   この機能は、ListPWACustomFields メソッドで実装されます。
    
2. プロジェクト ユーザー設定フィールドと非カスタム フィールドを取得します。
    
   ECFs でプロジェクトを取得するとき、プロジェクトのオンライン サービスにクエリ要求を次の項目を含める必要があります。 
    
   - **IncludeCustomFields**&ndash;は、この項目が公開されている各プロジェクトにユーザー設定フィールドをサポートしている拡張機能が含まれている PublishedProjects のコレクションを取得するサービスを要求します。 この項目が指定されている場合を除き、オンラインのプロジェクト オブジェクトを返します PublishedProject カスタム フィールドのデータが含まれていません。
    
   - **IncludeCustomFields.CustomFields** &ndash;は、この項目名のデータを PublishedProject オブジェクトを作成するサービスを要求します。
    
   次のような要求は、プロジェクトの Id と、ユーザー設定フィールドのオブジェクトの拡張機能とユーザー設定フィールドの値を指定します。
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. 各プロジェクトを確認します。
    
   このアプリケーションで使用されているプロジェクトのオブジェクトは、値の取得および表示するための PublishedProject 型です。 
    
   1 つまたは複数のプロジェクト内のデータ値を更新する場合は、更新プログラムを実行中のプロジェクトをチェック アウト、およびアプリケーションでは、DraftProject オブジェクトを使用して値を取得し、プロジェクトを更新するのには。
    
4. プロジェクトの ECF エントリへのアクセス
    
   ECF ごとでは、ECF の情報の残りの部分からフィールドの値を区切ります。 フィールドの値は、キー/値のペアの一部として格納されます。 情報の残りの部分は、カスタム オブジェクトに格納されます。
    
   ECF の値にアクセスするプロジェクトは、2 つの部分で構成されます。
    
   - 名のコレクションを循環させる
    
   - 2 つの構造を使用して、適切なエントリにアクセスします。
    
   各プロジェクト名のコレクションは、列挙可能な 2 つの場所で ECF の関連するエントリを格納して、キーと値のペアの一部としてフィールドの値です。 、キー/値のペアで、internalName キーは、フィールドの値は、値です。 保持し、フィールド値にアクセスするには、辞書を使用します。 
    
   ECF プロパティ、フィールドの値以外は、プロジェクトごとに 1 つのオブジェクトに、カスタム オブジェクトに格納されます。 個々 のプロジェクトに関連付けられている ECFs にアクセスするのにには、名のコレクションを使用します。 
    
5. 各プロジェクトでは、ECF の各エントリが、キー、ECF--と、ECF の値を保持するオブジェクトの内部名で構成されているコレクションに関連付けられている ECFs を格納します。 コレクションを個別のエントリにアクセスするための辞書に転送します。 宣言に依存します。
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   ディクショナリ エントリの値は、ECF のデータ型に対応しています。 各 ECF のオブジェクトは、さまざまな種類の 1 つにマップします。 ほとんどの ECFs は、標準的な変数に格納する単純型を使用します。 次のフラグメントは、いくつかの種類の最小限の処理が含まれていることを示しています。
    
   ```cs
    switch (cf.FieldType)
    {
        case CustomFieldType.COST:
            decimal costValue = (decimal)oVal;
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                costValue.ToString("C"));
            break;
        case CustomFieldType.DATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FINISHDATE:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.DURATION:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.FLAG:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
        case CustomFieldType.NUMBER:
            Console.WriteLine("\tFieldType:\t{0}\n\tValue:\t{1}", cf.FieldType, 
                oVal.ToString());
            break;
    
   ```

   テキストの値のルックアップ テーブルには、ただし、追加の処理が必要です。 アプリケーションでは、サービスから適切な参照テーブルを取得し、参照テーブルを走査して、ECF のインスタンス (1 つまたは複数の値) を出力します。 次のコードは、テキスト ECFs などの単純な値を持つルックアップ テーブルを使用してこれらの処理を示しています。 
    
   ```cs
    case CustomFieldType.TEXT:
        if (!cf.LookupTable.ServerObjectIsNull.HasValue ||
            (cf.LookupTable.ServerObjectIsNull.HasValue && 
            cf.LookupTable.ServerObjectIsNull.Value))
        { //No lookup table
            Console.WriteLine("\tFieldType:\t{0}\n\tText:\t{1}", cf.FieldType, 
                oVal.ToString());
        }
        else
        { //Lookup table
            Console.WriteLine("\tFieldType:\t{0} - using Lookup Table", cf.FieldType);
            String[] entries = (String[])oVal;
            foreach (String entry in entries)
            {
                var luEntry = projContext.LoadQuery(cf.LookupTable.Entries
                    .Where(e => e.InternalName == entry));
                projContext.ExecuteQuery();
                Console.WriteLine("\tLookup Value:\t{0}", luEntry.First().FullValue);  
            }
        }
        break;
    
   ```

   このアプリケーションだけでは値を出力します。ただし、データ値の複数の意味を取得することができます。
    
## <a name="listpwacustomfields"></a>ListPWACustomFields

ListPWACustomFields メソッドは、取得し、プロジェクトに関連付けられている ECFs を一覧表示します。 このメソッドは、個々 のプロジェクトに関連付けることができる PWA のインスタンスに登録されている ECFs を一覧表示します。 ECFs にアクセスするためのエントリ ポイントでは、クエリ要求を次のように、プロジェクトのコンテキストの要素名を使用します。
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

メソッドは、プロジェクトが特定の ECF を使用するかどうかを確認するのにはチェックされません。
  
## <a name="see-also"></a>関連項目

- [プロジェクト開発のポータル](https://developer.microsoft.com/en-us/project)
- [概要: エンタープライズ ユーザー設定フィールドと参照テーブル](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- [ローカル ユーザー設定フィールドとエンタープライズ ユーザー設定フィールド](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)
- [Project Server 2013 でのエンタープライズ ユーザー設定フィールドを追加または更新](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    


---
title: Project Online エンタープライズ ユーザー設定フィールドへのアクセス
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 25509631-fa14-49d8-b594-cfacf5355c38
description: Project Online は、企業がビジネス ニーズを満たすように拡張できる Office 365 サービスの 1 つです。 1 つの拡張領域は、エンタープライズ ユーザー設定フィールド (ECF) です。 ECF は、プロジェクト、リソース、およびタスクに追加できる型指定された値フィールドです。 次の表に、プロジェクト、リソース、およびタスクに関連付けられた ECF のリストと、その ECF のインスタンスに対応する値の例を示します。
localization_priority: Priority
ms.openlocfilehash: 9f754f1446890ae021bf6f7000ffba11e2a2df33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355084"
---
# <a name="accessing-project-online-enterprise-custom-fields"></a>Project Online エンタープライズ ユーザー設定フィールドへのアクセス

Project Online は、企業がビジネス ニーズを満たすように拡張できる Office 365 サービスの 1 つです。 1 つの拡張領域は、エンタープライズ ユーザー設定フィールド (ECF) です。 ECF は、プロジェクト、リソース、およびタスクに追加できる型指定された値フィールドです。 次の表に、プロジェクト、リソース、およびタスクに関連付けられた ECF のリストと、その ECF のインスタンスに対応する値の例を示します。
  
|ECF 名|ECF 型|関連付け|値の例|
|:-----|:-----|:-----|:-----|
|妥当性  <br/> |TEXT  <br/> |プロジェクト  <br/> |エンド ユーザーは、人口統計と健康データと共に、健康評価およびより良い健康状態に向けた個別の行動計画を含む結果を記録できます。  <br/> |
|リスクの評価  <br/> |TEXT  <br/> |プロジェクト  <br/> |低  <br/> |
|ROI  <br/> |NUMBER  <br/> |プロジェクト  <br/> |2.10  <br/> |
|総コスト  <br/> |COST  <br/> |プロジェクト  <br/> |$1,031,514  <br/> |
|チームの立ち上げ  <br/> |TEXT  <br/> |リソース  <br/> |はい  <br/> |
|役職  <br/> |TEXT  <br/> |リソース  <br/> |テスト担当者  <br/> |
|フラグの状態  <br/> |FLAG  <br/> |タスク  <br/> |いいえ  <br/> |
|正常性  <br/> |TEXT  <br/> |タスク  <br/> |指定なし  <br/> |
   
ECF は、プロジェクト、リソース、またはタスクの外部にある Project Web アプリケーション (PWA) インスタンスで定義されます。 それにもかかわらず、プロジェクト、リソース、またはタスクに関連付けることもできます。 この記事では、サンプル アプリケーションを使用してユーザー設定フィールドの初歩的な概要を示します。特に、ECF 値の取得について重点的に説明します。 
  
完全なサンプルは、https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields でダウンロードできます。
  
さらに、Project Online は、特定のプロジェクト、リソース、またはタスクに固有の読み取り専用エンティティとして、ローカル ユーザー設定フィールドもサポートしています。 ローカル ユーザー設定フィールドの詳細については、サンプル https://github.com/OfficeDev/Project-CSOM-Read-Local-CustomFields\ を参照してください。
  
## <a name="background-materials"></a>背景資料

前の記事「[クライアント側オブジェクト モデルを使用した Project Online アプリケーションの開発](developing-a-project-online-application-using-the-client-side-object-model.md)」では、CSOM を使用してアプリケーションを開発する際の背景と初期方針について説明しています。 次の項目については、この記事を参照してください。
  
- Project のスタンドアロン エディションとクラウドベース エディションに関する背景情報 
    
- 開発環境 (Visual Studio のエディションとソフトウェア ライブラリ)
    
- CSOM ライブラリを使用する .NET アプリケーション用の Visual Studio プロジェクトの設定
    
- Project Online サービスへの接続
    
## <a name="preliminaries-class-level-declarations"></a>準備 (クラスレベルの宣言)

このアプリケーションのクラスでは、2 つのデータ項目 (プロジェクト コンテキストと pwaECF ディクショナリ) を定義します。
  
プロジェクト コンテキスト オブジェクトは、Project CSOM の一部であり、アプリケーションと PWA インスタンスを接続します。 サービスに対するすべての要求で、プロジェクト コンテキストを使用します。
  
```cs
private static ProjectContext projContext = 
     new ProjectContext("https://Contoso216.sharepoint.com/sites/pwa");

```

このコンテキストには、アプリケーションでインスタンスを作成するための接続エンドポイントが必要です。 この接続エンドポイントは、PWA インスタンスの URL になります。 
  
pwaECF ディクショナリには、PWA レベルで定義したプロジェクトの ECF を保存します。 このディクショナリは、キーとして ECF.InternalName を使用し、値として CustomField オブジェクトを使用します。 ディクショナリのデータは ListPWACustomFields メソッドで設定され、Main メソッドでリファレンスとして使用されます。 
  
```cs
    //Dictionary of ECFs
        static Dictionary<String, CustomField> pwaECF = new Dictionary<string, CustomField>();

```

## <a name="main-method"></a>Main メソッド

Main メソッドでは、アプリケーション フローを管理します。 Project Online CSOM を使用する他のアプリケーションと同様に、Main でプロジェクト コンテキストを初期化します。 
  
1. Project Online PWA の ECF を取得してリスト表示します。
    
   この機能は、ListPWACustomFields メソッドに実装されています。
    
2. ユーザー設定フィールドと非ユーザー設定フィールドを含むプロジェクトを取得します。
    
   ECF を含むプロジェクトの取得時には、Project Online へのクエリ要求に次の項目を含める必要があります。 
    
   - **IncludeCustomFields** &ndash; この項目では、それぞれの発行済みプロジェクトにユーザー設定フィールドをサポートする拡張機能が含まれている PublishedProjects のコレクションを返すようにサービスに要求します。 この項目が指定されていないと、Project Online はユーザー設定フィールドのデータを含まない PublishedProject オブジェクトを返します。
    
   - **IncludeCustomFields.CustomFields** &ndash; この項目では、CustomFields データで PublishedProject オブジェクトのデータを設定するようにサービスに要求します。
    
   次の要求では、プロジェクトの ID と名前、およびユーザー設定フィールドとユーザー設定フィールド値のオブジェクト拡張機能を指定しています。
    
   ```cs
        var projBlk = projContext.LoadQuery(
        projContext.Projects.Include(
            p => p.Id, 
            p => p.Name,
            p => p.IncludeCustomFields,
            p => p.IncludeCustomFields.CustomFields
        ));
    
   ```

3. それぞれのプロジェクトを確認します。
    
   このアプリケーションで使用しているプロジェクトのオブジェクトは、値を取得して表示するために、PublishedProject 型になっています。 
    
   1 つまたは複数のプロジェクトのデータ値を更新する必要がある場合、更新中のプロジェクトはチェック アウトされ、アプリケーションは値の取得とプロジェクトの更新に DraftProject オブジェクトを使用するようになります。
    
4. プロジェクトの ECF エントリを割り当てます
    
   それぞれの ECF によって、フィールド値がそれ以外の情報と分離されます。 フィールド値は、キーと値のペアの一部分として保存されます。 それ以外の情報は、CustomField オブジェクトに保存されます。
    
   2 つの部分で構成されるプロジェクトの ECF 値にアクセスする方法:
    
   - CustomFields コレクションを繰り返し処理します
    
   - 2 つのコンストラクターを使用して適切なエントリにアクセスします。
    
   それぞれのプロジェクトが、関連付けられた ECF エントリを 2 つの場所 (列挙可能な CustomFields コレクションと、キー/値ペアの一部としてのフィールド値) に保存します。 キー/値ペアでは、internalName がキーになり、フィールド値が値になります。 フィールド値の保持とアクセスには、ディクショナリを使用します。 
    
   ECF のプロパティ (フィールド値以外) は、プロジェクトごとに 1 つの CustomField オブジェクトに保存されます。 CustomFields コレクションを使用して、それぞれ個別のプロジェクトに関連付けられた ECF にアクセスします。 
    
5. それぞれのプロジェクトは、それに関連付けられた ECF をコレクションに保存します。このコレクションの各 ECF エントリは、ECF の内部名であるキーと ECF の値を保持するオブジェクトで構成されています。 このコレクションは、それぞれのエントリにアクセスするためのディクショナリに転送します。 宣言は次のとおりです。
    
   ```cs
    Dictionary<string, object> projDict = pubProj.IncludeCustomFields.FieldValues;
    
   ```

   ディクショナリ エントリの値は、ECF のデータ型に相当します。 それぞれの ECF のオブジェクトは、さまざまな型の 1 つにマップします。 ほとんどの ECF は、標準的な変数に適合する単純型を使用します。 次のフラグメントは、いくつかの型に関連する最小限の処理を示しています。
    
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

   ただし、TEXT 値の参照テーブルには、追加の処理が必要になります。 アプリケーションは、サービスから適切な参照テーブルを取得し、その参照テーブルを調べることで ECF インスタンスを (単一または複数の値と共に) 出力します。 次のコード フラグメントは、単純な値を保持するものと参照テーブルを使用するものを含む TEXT ECF の処理を示しています。 
    
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

   このアプリケーションでは、単に値を出力していますが、データの値からより多くの意味を得ることも可能です。
    
## <a name="listpwacustomfields"></a>ListPWACustomFields

ListPWACustomFields メソッドでは、プロジェクトに関連付けられた ECF を取得してリスト表示します。 このメソッドは、個別のプロジェクトに関連付けできる PWA インスタンスに登録された ECF をリスト表示します。 ECF にアクセスするためのエントリ ポイントは、次のクエリ要求に示すように、プロジェクト コンテキストの CustomFields 要素を使用します。
  
```cs
// Project ECFs
    var allECFields = 
            projContext.LoadQuery(projContext.CustomFields.Include(
            qp => qp.InternalName,
            qp => qp.Name
        ));
    projContext.ExecuteQuery();

```

このメソッドでは、プロジェクトが特定の ECF を使用しているかどうかを確認していません。
  
## <a name="see-also"></a>関連項目

- [Project 開発ポータル](https://developer.microsoft.com/ja-JP/project)
- 
  [概要: エンタープライズ ユーザー設定フィールドと参照テーブル](https://support.office.com/en-us/article/overview-enterprise-custom-fields-and-lookup-tables-f99db553-0b33-4648-93c0-f6a74637d790?ui=en-us&rs=en-us&ad=us)
- [ローカル ユーザー設定フィールドとエンタープライズ ユーザー設定フィールド](https://msdn.microsoft.com/library/office/ms447495(v=office.14).aspx)
- [Project Server 2013 でエンタープライズ ユーザー設定フィールドを追加または編集する](https://docs.microsoft.com/project/add-or-edit-enterprise-custom-fields-in-project-server)
    


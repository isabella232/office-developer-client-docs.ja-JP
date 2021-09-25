---
title: LookupRecord Data Block (Access custom Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: LookupRecord データ ブロックは、特定のレコードに対して一連のアクションを実行します。
ms.openlocfilehash: 76020c4afc9188a432f78fd78bed56aa8096e67c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605793"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>LookupRecord Data Block (Access custom Web app)

A **LookupRecord** data block performs a set of actions on a specific record. 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> LookupRecord  データ ブロックは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>設定

**LookupRecord** アクションの引数は次のとおりです。 
  
|**引数**|**必須**|**説明**|
|:-----|:-----|:-----|
| _In_ <br/> |必要  <br/> |操作するレコードを識別する文字列を指定します。 *In 引数* には、テーブルの名前、選択クエリ、またはクエリ ステートメントSQLできます。  <br/> |
| Where Condition/Where 条件式 <br/> |いいえ  <br/> |**LookupRecord** データ ブロックを適用するデータの範囲を制限する文字列式を指定します。 たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。 criteria を省略すると **、LookupRecord** データ ブロックは In 引数で指定されたドメイン全体で  *動作*  します。 条件に含まれるフィールドは、In のフィールドである必要  *があります*  。  <br/> |
| _Alias_ <br/> |いいえ  <br/> |In 引数で指定されたレコードの代替名を指定  *する文字列*  。 以降の参照用にテーブル名を短くして、あいまいな参照を防ぐ目的でよく使用されます。 Alias  *を*  指定しない場合、テーブル名またはクエリ名がエイリアスとして使用されます。  <br/> |
   
## <a name="remarks"></a>注釈

If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record. 
  
If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value. 
  


---
title: LookupRecord Data Block (Access custom Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: LookupRecord データ ブロックは、特定のレコードに対して一連のアクションを実行します。
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434362"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>LookupRecord Data Block (Access custom Web app)

A **LookupRecord** data block performs a set of actions on a specific record. 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> LookupRecord  データ ブロックは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>Setting

**LookupRecord** アクションの引数は次のとおりです。 
  
|**引数**|**必須**|**説明**|
|:-----|:-----|:-----|
| _In_ <br/> |はい  <br/> |操作するレコードを識別する文字列を指定します。 *In 引数* には、テーブルの名前、選択クエリ、またはクエリ ステートメントSQLできます。  <br/> |
| Where Condition/Where 条件式 <br/> |いいえ  <br/> |**LookupRecord** データ ブロックを適用するデータの範囲を制限する文字列式を指定します。 たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。 criteria を省略すると **、LookupRecord** データ ブロックは In 引数で指定されたドメイン全体で  *動作*  します。 条件に含まれるフィールドは、In のフィールドである必要  *があります*  。  <br/> |
| _Alias_ <br/> |いいえ  <br/> |In 引数で指定されたレコードの代替名を指定  *する文字列*  。 以降の参照用にテーブル名を短くして、あいまいな参照を防ぐ目的でよく使用されます。 Alias  *を*  指定しない場合、テーブル名またはクエリ名がエイリアスとして使用されます。  <br/> |
   
## <a name="remarks"></a>注釈

If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record. 
  
If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value. 
  


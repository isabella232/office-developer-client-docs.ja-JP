---
title: ForEachRecord データ ブロック (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: ForEachRecord データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428236"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>ForEachRecord データ ブロック (Access カスタム Web アプリ)

**ForEachRecord** データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> **ForEachRecord** データ ブロックは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>Setting

"**ForEachRecord**/レコードごと" アクションの引数は次のとおりです。 
  
|**引数名**|**必須**|**説明**|
|:-----|:-----|:-----|
|**In** <br/> |はい  <br/> |実行するステートメントの対象レコードのドメインを識別する文字列。 *In 引数* には、テーブルの名前、選択クエリ、またはクエリ ステートメントSQLできます。  <br/> **注**: 指定したドメインには、リンク テーブルまたは ODBC データ ソースに格納されているデータを含めできません。           |
|Where Condition/Where 条件式 <br/> |いいえ  <br/> |**ForEachRecord** データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。 たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。 criteria を省略すると、引数 In で指定されたドメイン全体で **ForEachRecord** データ ブロックが  *動作*  します。 条件に含まれるフィールドは、In のフィールドである必要  *があります*  。  <br/> |
|**Alias** <br/> |いいえ  <br/> |In 引数で指定されたドメインの代替名を指定  *する文字列*  。 以降の参照用にテーブル名を短くして、あいまいな参照を防ぐ目的でよく使用されます。 Alias  *を*  指定しない場合、テーブル名またはクエリ名がエイリアスとして使用されます。  <br/> |
   
## <a name="remarks"></a>注釈

Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately. 
  


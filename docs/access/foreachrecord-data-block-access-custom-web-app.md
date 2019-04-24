---
title: ForEachRecord データブロック (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: ForEachRecord データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302458"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>ForEachRecord データブロック (Access カスタム web アプリ)

**ForEachRecord** データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。 
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> **ForEachRecord** データ ブロックは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>Setting

"**ForEachRecord**/レコードごと" アクションの引数は次のとおりです。 
  
|**引数名**|**必須**|**説明**|
|:-----|:-----|:-----|
|**順番** <br/> |はい  <br/> |実行するステートメントの対象レコードのドメインを識別する文字列。 引数*In に*は、テーブル名、選択クエリ、または SQL ステートメントを含めることができます。  <br/> **注**: 指定されたドメインには、リンクテーブルまたは ODBC データソースに格納されているデータを含めることはできません。           |
|Where Condition/Where 条件式 <br/> |いいえ  <br/> |**ForEachRecord** データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。 たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。 criteria を省略すると、引数*In で*指定したドメイン全体で**ForEachRecord**データブロックが動作します。 抽出条件に含まれているフィールドは、のフィールドで** もある必要があります。  <br/> |
|**Alias** <br/> |いいえ  <br/> |引数*In で*指定したドメインの代替名を示す文字列型 (string) の値を使用します。 以降の参照用にテーブル名を短くして、あいまいな参照を防ぐ目的でよく使用されます。 *alias*が指定されていない場合は、テーブル名またはクエリ名がエイリアスとして使用されます。  <br/> |
   
## <a name="remarks"></a>解説

Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately. 
  


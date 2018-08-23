---
title: ForEachRecord データ ブロック (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: ForEachRecord データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798590"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>ForEachRecord データ ブロック (カスタム web アプリケーションのアクセス)

**ForEachRecord** データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> [!メモ] **ForEachRecord** データ ブロックは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>設定

" **ForEachRecord** /レコードごと" アクションの引数は次のとおりです。 
  
|**引数名**|**必須**|**説明**|
|:-----|:-----|:-----|
|**で** <br/> |はい  <br/> |操作対象のレコードのドメインを識別する文字列です。 ** 引数は、テーブル、選択クエリ、または SQL ステートメントの名前を含めることができます。  <br/> **注**: 指定されたドメインにリンクされているテーブルまたは ODBC データ ソースに格納されたデータを含めることはできません。           |
|**Where Condition** <br/> |いいえ  <br/> |**ForEachRecord**データ ブロックのデータの範囲を制限するために使用する文字列式を実行するとします。 抽出条件を指定する SQL 式の WHERE 句にはあります。 条件は省略すると、 **ForEachRecord**データ ブロック*に*引数で指定されたドメイン全体で動作します。 条件に含まれる任意のフィールドは、フィールド*内*にもあります。  <br/> |
|**エイリアス** <br/> |いいえ  <br/> |** 引数で指定されたドメインの代替名を提供する文字列です。 あいまいな参照を防ぐへの参照のテーブル名を短くには、よく使用されます。 *エイリアス*が指定されていない場合、テーブルまたはクエリの名前がエイリアスとして使用します。  <br/> |
   
## <a name="remarks"></a>注釈

[ForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md) データ ブロックを即座に終了するには、" ****ExitForEachRecord/レコードごとに終了**** " アクションを使用します。 
  


---
title: 制限の種類
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3fd12f2bed213bf48db18b8dacafc8d522439140
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590899"
---
# <a name="types-of-restrictions"></a>制限の種類

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
制限には多くの種類があります。特定の列に焦点を当てたものがあります。 すべてのテーブル実装は、現在の列セット内の列に対する制限をサポートする必要があります。 ただし、値を追加するために、テーブルの実装者は、現在テーブル ビューに含けられていないオブジェクト プロパティに基づく制限をサポートできます。
  
一部の制限は、論理 **AND、OR、****または NOT** 操作を実行する制限を使用して **組み合** わせることができます。 たとえば、ほとんどのプロパティ制限は **、AND** 制限を使用して存在する制限と結合する必要があります。 プロパティ制限で使用されるプロパティが **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティである場合や、テーブル内の必須列である場合など、いくつかの例外があります。 MAPI は、プロパティが存在しない場合にサービス プロバイダーがプロパティ制限を評価する方法を指定していないので、ビューを制限するクライアントの構築制限は、プロパティ制限に存在する制限を使用する必要があります。 サービス プロバイダーが制限に失敗したが、要件がないのは妥当であり、お勧めします。 
  
制限は、より特殊な制限構造の共用体と、共用体に含まれる構造の種類のインジケーターを含む [SRestriction](srestriction.md) データ構造を使用して定義されます。 
  
共用体の特殊な制限構造は、それぞれ異なる種類の制限を表します。 制限の種類と関連するデータ構造は次のとおりです。
  
|**制限の種類**|**関連付けられたデータ構造**|**説明**|
|:-----|:-----|:-----|
|Compare プロパティ  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |同じ種類の 2 つのプロパティを比較します。  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |2 つ以上の **制限に** 対して論理 AND 操作を実行します。  <br/> |
|**OR** <br/> |[SOrRestriction](sorrestriction.md) <br/> |2 つ以上の **制限に** 対して論理 OR 操作を実行します。  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |2 つ以上の **制限に対して** 論理 NOT 操作を実行します。  <br/> |
|Content  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |指定したデータを検索します。  <br/> |
|プロパティ  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |一致する条件として特定のプロパティ値を指定します。 たとえば、特定の種類の添付ファイルを検索するために使用できます。  <br/> |
|Bitmask  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |ビットマスクを PT_LONGプロパティに適用します。通常、特定のフラグが設定されているかどうかを判断します。  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |標準の関係演算子を使用してプロパティのサイズをテストします。  <br/> |
|Exist  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |オブジェクトにプロパティの値が含されているかどうかをテストします。  <br/> |
|サブオブジェクト  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |サブオブジェクト、または受信者や添付ファイルなどのエントリ識別子でアクセスできないオブジェクトを検索するために使用されます。 たとえば、特定の受信者のメッセージを検索するために使用できます。  <br/> |
|コメント  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |オブジェクトを名前付きプロパティのセットに関連付ける。  <br/> |
   
一部の制限では正規表現が使用され、MAPI は、多くのテキスト アプリケーションで使用されるスタイルで、限られた形式の正規表現表記をサポートします。
  
コメント制限は、アプリケーション固有の情報を制限に保持するためにディスクに制限を保存するクライアントによって使用されます。 たとえば、プロパティ制限で使用される名前付きプロパティの名前を保存するクライアントは、コメント制限を使用してこれを行います。 プロパティの制限では、名前を保存できない。 [SPropertyRestriction データ構造](spropertyrestriction.md) は、プロパティ タグのみを保持します。 コメント制限は[IMAPITable::Restrict](imapitable-restrict.md)によって無視され、Restrict 呼び出しが行われた後に[IMAPITable::QueryRows](imapitable-queryrows.md)によって返される行には影響しません。  
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)


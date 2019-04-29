---
title: 制限の種類
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 28159dfb947b4fb0ea54680627588b7c10bee3b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416287"
---
# <a name="types-of-restrictions"></a>制限の種類

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の列に焦点を当てる制限には、さまざまな種類があります。 すべてのテーブル実装は、現在の列セットの列の制限をサポートすることが期待されています。 ただし、テーブルの実装では、テーブルビューに現在含まれていないオブジェクトのプロパティに基づく制限をサポートすることもできます。
  
一部の制限は、 **and**、 **or**、 **NOT**の論理演算を実行する制限を使用して組み合わせることができます。 たとえば、ほとんどのプロパティ制限は、**および**制限を使用して、存在する制限と結合する必要があります。 プロパティ制限で使用されるプロパティが**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティである場合や、テーブルの必須の列である場合など、いくつかの例外があります。 プロパティが存在しない場合、MAPI では、サービスプロバイダーがプロパティの制限を評価する方法を指定していないため、ビューを制限するクライアント構築の制限は、プロパティ制限によって存在する制限を使用する必要があります。 サービスプロバイダーが制限を満たさないことをお勧めしますが、要件はありません。 
  
制限は、 [srestriction](srestriction.md)データ構造を使用して定義されています。これには、より特殊な制限構造の和集合と、ユニオンに含まれる構造の種類のインジケーターが含まれています。 
  
共用体の特殊な制限の各構造体は、異なる種類の制限を表します。 制限の種類とそれに関連付けられているデータ構造は次のとおりです。
  
|**制限の種類**|**関連付けられたデータ構造**|**説明**|
|:-----|:-----|:-----|
|Compare プロパティ  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |同じ種類の2つのプロパティを比較します。  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |2つ以上の制限に対して論理**AND**操作を実行します。  <br/> |
|**または** <br/> |[SOrRestriction](sorrestriction.md) <br/> |2つ以上の制限に対して論理**or**操作を実行します。  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |2つ以上の制限で、論理**NOT**操作を実行します。  <br/> |
|コンテンツ  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |指定したデータを検索します。  <br/> |
|プロパティ  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |特定のプロパティ値を一致条件として指定します。 たとえば、特定の種類の添付ファイルを検索する場合などに使用できます。  <br/> |
|示す  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |PT_LONG プロパティにビットマスクを適用します。通常は、特定のフラグが設定されているかどうかを判断します。  <br/> |
|サイズ  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |標準の関係演算子を使用して、プロパティのサイズをテストします。  <br/> |
|ない  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |オブジェクトにプロパティの値があるかどうかをテストします。  <br/> |
|サブ  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |サブオブジェクト、または受信者や添付ファイルなどのエントリ識別子でアクセスできないオブジェクトを検索するために使用されます。 たとえば、特定の受信者のメッセージを検索する場合などに使用できます。  <br/> |
|Comment  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |オブジェクトを一連の名前付きプロパティに関連付けます。  <br/> |
   
一部の制限は正規表現を使用します。 MAPI では、多くのテキストアプリケーションで使用されているスタイルでの正規表現表記の制限付き形式をサポートしています。
  
コメント制限は、アプリケーション固有の情報を制限として保持するためにディスクに制限を保存するクライアントによって使用されます。 たとえば、プロパティ制限で使用される名前付きプロパティの名前を保存するクライアントは、コメント制限を使用できます。 プロパティ制限で名前を保存することはできません。[spropertyrestriction](spropertyrestriction.md)データ構造には、property タグのみが保持されます。 コメント制限は[imapitable:: restrict](imapitable-restrict.md)では無視されます。制限呼び出しが行われた後、 [imapitable:: QueryRows](imapitable-queryrows.md)によって返される行には影響しません。 **** 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)


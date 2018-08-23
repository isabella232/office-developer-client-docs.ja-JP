---
title: 制限の種類
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 85cf254c9ea23ecbd6f311ba012d2e048a0b2a6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572446"
---
# <a name="types-of-restrictions"></a>制限の種類

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
上にある多くの種類の制限の一部対象とする特定の列。 テーブルのすべての実装は、現在の列セットの列の制限をサポートする必要があります。 ただし、値を追加するには、テーブルの実装もサポートできます、現在のテーブル ビューにないオブジェクトのプロパティに基づいて制限。
  
論理**AND**、**または**、または**しない**操作を実行するための制限では、いくつかの制限を組み合わせて指定できます。 などと制限を結合する必要がありますほとんどのプロパティでは、**および**制限を使用して制限が存在します。 プロパティ制限で使用されるプロパティが、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) のプロパティである場合など、またはテーブル内の必要な列がある場合、いくつかの例外があります。 使用があるはずのプロパティの制限の制限 MAPI では、サービス ・ プロバイダーが評価方法プロパティ制限のプロパティが存在しない場合は指定しないため、表示を制限する制約を作成するクライアントです。 妥当、サービス プロバイダーが失敗、制限が存在しない要件をお勧めします。 
  
制限を定義するより専門的な制限の構造体の共用体と構造体、共用体での種類を示すインジケーターが含まれている[SRestriction](srestriction.md)データ構造体を使用します。 
  
各特殊な制限構造体、共用体では、制限の種類を表します。 制約、およびそれらに関連付けられているデータ構造体の型は次のとおりです。
  
|**制限の種類**|**関連付けられているデータの構造**|**説明**|
|:-----|:-----|:-----|
|プロパティを比較します。  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |同じ型の 2 つのプロパティを比較します。  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |制限の 2 つ以上の論理**AND**演算を実行します。  <br/> |
|**または** <br/> |[SOrRestriction](sorrestriction.md) <br/> |制限の 2 つ以上の論理**OR**演算を実行します。  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |制限の 2 つ以上の論理**NOT**演算を実行します。  <br/> |
|Content  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |指定されたデータを検索します。  <br/> |
|プロパティ  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |照合のための条件として、特定のプロパティ値を指定します。 使用できます、たとえば、特定の種類の添付ファイルを検索します。  <br/> |
|Bitmask  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |特定のフラグが設定されているかどうかを判断するのには通常、PT_LONG プロパティに 1 を適用します。  <br/> |
|サイズ  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |標準の関係演算子を使用してプロパティのサイズをテストします。  <br/> |
|存在  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |オブジェクトがプロパティの値を持つかどうかをテストします。  <br/> |
|サブオブジェクト  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |下位オブジェクト、またはエントリ id、受信者や添付ファイルなどにアクセスできないオブジェクトを検索するために使用します。 使用できます、たとえば、特定の受信者のメッセージを検索します。  <br/> |
|Comment  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |名前付きプロパティのセットを使用してオブジェクトに関連付けます。  <br/> |
   
いくつかの制限は、正規表現を使用し、MAPI は、制限された形式をサポートしている正規表現の表記されているスタイルではテキストの多くのアプリケーションを使用します。
  
コメントの制限は、制限された、アプリケーション固有の情報を保持するディスク上の制限を保存するクライアントによって使用されます。 たとえば、プロパティ制限で使用される名前付きプロパティの名前を保存するクライアントこれを行うコメントの制限を持つ。 名前を保存をすることはありません; プロパティ制限で使用可能です[SPropertyRestriction](spropertyrestriction.md)データ構造体は、プロパティ タグのみを保持します。 コメントの制限は、**制限する**呼び出しが行われた後、 [IMAPITable::QueryRows](imapitable-queryrows.md)によって返される行には影響があるないという点で、 [IMAPITable::Restrict](imapitable-restrict.md)で無視されます。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)


---
title: MAPI プロパティタグ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328238"
---
# <a name="mapi-property-tags"></a>MAPI プロパティタグ
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティタグは、次の図に示すように、ビット 16 ~ 31 の一意のプロパティ識別子と、ビット 0 ~ 15 のプロパティの種類を含む32ビットの数値です。 
  
**プロパティ タグ要素**
  
![Property タグ要素](media/amapi_10.gif "Property タグ要素")
  
プロパティタグは mapi プロパティを識別するために使用され、プロパティが mapi、クライアント、またはサービスプロバイダーのどちらで定義されているかに関係なく、すべてのプロパティが必要です。 MAPI では、Mapitags ヘッダーファイルのプロパティの一連のプロパティタグ定数が定義されています。これらのプロパティは、"MAPI で定義されたプロパティ" と呼ばれます。 
  
property tag 定数は、一貫性と使いやすさのための命名規則に従います。 各 property タグの名前には、PR_ プレフィックスと、プロパティの内容を記述する1つ以上の文字列があります。 複数の文字列は、アンダースコアで区切られています。 たとえば、メッセージ受信者のアドレスの種類のプロパティタグは**PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) で、すべての送信メッセージのコピーを受信するように指定されたフォルダーのエントリ識別子は**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))。
  
[PROP_TYPE](prop_type.md)、 [PROP_ID](prop_id.md)、および[PROP_TAG](prop_tag.md)の中から、プロパティタグの操作に役立つマクロがいくつか用意されています。 **PROP\_型**プロパティタグからプロパティの種類を抽出します。**PROP\_id**は識別子を抽出します。 **PROP_TAG**は、プロパティの型と識別子からプロパティタグを作成します。 
  
## <a name="see-also"></a>関連項目

- [MAPI のプロパティの概要](mapi-property-overview.md)


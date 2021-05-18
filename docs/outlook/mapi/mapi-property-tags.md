---
title: MAPI プロパティのタグ
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
# <a name="mapi-property-tags"></a>MAPI プロパティのタグ
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ タグは、ビット 16 ~ 31 の一意のプロパティ識別子と、次の図に示すように、ビット 0 ~ 15 のプロパティ型を含む 32 ビットの数値です。 
  
**プロパティ タグ要素**
  
![プロパティ タグ要素](media/amapi_10.gif "プロパティ タグ要素")
  
プロパティ タグは MAPI プロパティを識別するために使用され、プロパティが MAPI、クライアント、またはサービス プロバイダーによって定義されているかどうかに関係なく、すべてのプロパティに 1 つが必要です。 MAPI は、Mapitags.h ヘッダー ファイル内のプロパティのプロパティ タグ定数のセットを定義します。これらのプロパティは"MAPI 定義プロパティ" と呼ばれます。 
  
プロパティ タグの定数は、一貫性と使いやすさを確保するために名前付け規則に従います。 各プロパティ タグの名前には、1 つのプレフィックスとプロパティPR_説明する 1 つ以上の文字列の 2 つの部分があります。 複数の文字列はアンダースコアで区切られた文字列です。 たとえば、メッセージ受信者のアドレスの種類のプロパティ タグは **PR \_ ADDRTYPE** ([PidTagOrgAddrtype)](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)であり、すべての送信メッセージのコピーを受信するために指定されたフォルダーのエントリ識別子は **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)です。
  
プロパティ タグの操作に役立ついくつかのマクロを使用して、[](prop_type.md)プロパティ タグ、PROP_TYPE、PROP_ID、PROP_TAG。 [](prop_tag.md) [](prop_id.md) **PROP \_TYPE** は、プロパティ タグからプロパティの種類を抽出します。 **PROP \_ID は** 識別子を抽出します。 **PROP_TAG** 型と識別子からプロパティ タグを作成します。 
  
## <a name="see-also"></a>関連項目

- [MAPI のプロパティの概要](mapi-property-overview.md)


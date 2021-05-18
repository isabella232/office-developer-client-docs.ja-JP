---
title: プロパティ名とプロパティ セット
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328547"
---
# <a name="property-names-and-property-sets"></a>プロパティ名とプロパティ セット

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前付きプロパティの名前には、次の 2 つの部分があります。
  
- プロパティ セットを指定するグローバル一意識別子 (GUID)。
    
- Unicode 文字文字列または 32 ビットの数値。 
    
名前付きプロパティの名前については [、MAPINAMEID 構造を使用して説明](mapinameid.md) します。 この構造体には、プロパティ セット メンバー、数値形式または文字列形式で名前を指定するためのメンバー、および使用される形式を識別するためのメンバーが含まれます。 プロパティ セットはプロパティの名前の一部なので、省略可能ではありません。 MAPI では、クライアントとサービス プロバイダーが使用する複数のプロパティ セットを定義していますが、既存のプロパティ セットが不適切な場合は、新しいプロパティ セットを定義できます。 クライアントとサービス プロバイダーは [、CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) 関数を呼び出すことによって、独自のプロパティ セットを定義できます。 通常、これらのプロパティ セットはカスタム クライアント アプリケーション用に作成されます。 
  
MAPI のプロパティ セットは、次の定数で表されます。
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
プロパティ PS_MAPIは予約済みです。サービス プロバイダーは、名前付きプロパティ範囲の下に識別子を持つプロパティの名前を生成するために使用されます。 ipM PS_PUBLIC_STRINGSの名前付きプロパティに対してクライアントが使用するプロパティセットです。 PS_PUBLIC_STRINGS プロパティ セットの名前付きプロパティはクライアントのユーザー インターフェイスに表示されるので、IPC メッセージ クラスに属するメッセージなどの表示できないメッセージは、このプロパティ セットを使用して名前付きプロパティを作成しないようにする必要があります。 代わりに、メッセージ クラス固有の範囲でプロパティを作成し、0x6800を0x7FFF。
  
他のプロパティ セットには、通常、ルーティング リストのメンバーである受信者を示す名前付きプロパティが保持されます。 受信者リスト のプロパティに関連付けられているプロパティと同じ種類の情報を含むこれらのプロパティ セットのプロパティは、ターゲット メッセージング システムのマッピングを必要とするゲートウェイによって理解されます。 プロパティを記述するための情報は 5 種類あるため、MAPI では 5 つの異なるプロパティ セットが定義されています。 ルーティング リスト メンバーのアドレスとアドレスの種類を含める必要があるメッセージを送信するクライアントは、PS_ROUTING_EMAIL_ADDRESSES および PS_ROUTING_ADDRTYPE プロパティ セット内の各メンバーに名前付きプロパティを割り当てる。 これにより、外部メッセージング システムに送信するときに、アドレスとアドレスの種類が有効なままになります。
  
## <a name="see-also"></a>関連項目



[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)


---
title: MAPI プロパティ識別子の概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 725256a64cb7d55be494ba623247255dfe5936c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801421"
---
# <a name="mapi-property-identifier-overview"></a>MAPI プロパティ識別子の概要

  
  
**適用されます**: Outlook 
  
プロパティの識別子は、プロパティの使用を示すために使用される番号およびその責任者です。 プロパティ識別子は、MAPI によって範囲に分かれています。識別子が範囲に該当する場所は、その使用法と所有権を示します。 
  
プロパティ識別子の範囲は、0x0001 から 0 xffff まで実行されます。 0x0000 と 0 xffff のプロパティ識別子は、すべての場合、これらの識別子を未使用に残す必要があることを意味に予約されています。 MAPI によって定義されているプロパティの範囲は、0x0001 からから 0x3FFF を実行します。 これらのプロパティは、MAPI 定義のプロパティと呼ばれます。 メッセージと受信者のプロパティが属する範囲 0x7FFF を 0x4000 と、クライアントまたはサービス プロバイダーは、この範囲のプロパティを定義できます。 0x0001 に 0x7FFF の範囲内のプロパティは、タグ付きのプロパティと呼ばれます。 0x8000 を超える、名前付きプロパティ、または 32 ビットのグローバル一意識別子 (GUID) が、Unicode 文字の文字列または数値の値を含むプロパティと呼ばれるものの範囲です。 クライアントは、そのプロパティの設定をカスタマイズするのには、名前付きプロパティを使用できます。
  
サービス プロバイダーは、0x67FF から 0x67F0 の範囲で、セキュリティで保護されたプロファイル プロパティを定義できます。 プロファイルのプロパティは、パスワードなどの追加の保護を必要とする情報の使用をセキュリティで保護します。 これらのプロパティを非表示にし、暗号化します。 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドによって返されるプロパティの既定の一覧でセキュリティで保護されたプロパティが含まれているかどうかは、プロバイダーの実装によって異なります。 通常これらのプロパティは含まれません。 [IProfSect: IMAPIProp](iprofsectimapiprop.md)インターフェイスは、セキュリティで保護されたプロパティを含む、プロファイル セクションのプロパティにアクセスするために使用します。 
  
プロパティの範囲のいくつかの機能は、転送可能なプロパティまたはプロパティを nontransmittable に制限されます。 転送可能なプロパティは、メッセージに転送されます。nontransmittable プロパティは、メッセージは転送されません。 Nontransmittable プロパティには、通常、クライアントとサービス プロバイダーが現在のセッションで動作するだけの価値のある情報が含まれます。 これらのプロパティは必ずしも別のメッセージング システムとサービス ・ プロバイダーの別のセットに便利です。 転送可能なプロパティの概念は、トランスポート プロバイダーに主に適用されます。 かプロパティが送信できるかどうかを確認するのには、 **FIsTransmittable**マクロは、Mapitags.h ヘッダー ファイルで定義する、プロパティ タグを渡します。 
  
識別子の範囲の詳細については、[プロパティ識別子の範囲](property-identifier-ranges.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI Property Overview](mapi-property-overview.md)

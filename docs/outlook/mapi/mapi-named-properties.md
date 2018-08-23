---
title: MAPI ���O�t���v���p�e�B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5a6ba7af5e497ba59b43e9b80cfc9595961ed10e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579544"
---
# <a name="mapi-named-properties"></a>MAPI ���O�t���v���p�e�B
 
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI には、プロパティに名前を割り当てるため、これらの名前を一意の識別子にマップするため、および永続的なこのマッピングを行うための機能が用意されています。 識別子のマッピングへの永続的な名前は、セッション間でプロパティ名が有効なまま、です。
  
名前付きプロパティを定義するには、クライアントまたはサービス プロバイダーの名前になり[MAPINAMEID](mapinameid.md)構造体に格納します。 ための名前は、32 ビットのグローバルに一意の識別子または GUID、およびどちらか、Unicode 文字の文字列または数値の値、名前付きプロパティの作成者は、重複除外を恐れることがなく意味のある名前を作成できます。 名が一意では、それらの識別子の値に関係なく使用できます。 
  
名前付きプロパティをサポートするためにサービス ・ プロバイダーは 2 つのメソッドを実装する: [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)と[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) -の名前と識別子の間で変換して、 [IMAPIProp::GetProps](imapiprop-getprops.md) [を許可するにはIMAPIProp::SetProps](imapiprop-setprops.md)を取得し、名前付きプロパティの範囲内で識別子とプロパティを変更するためのメソッドです。 名前付きプロパティの識別子の範囲は 0x8000 から 0 xfffe までの間です。 
  
**IMAPIProp**インターフェイスを実装する任意のオブジェクトは、名前付きプロパティをサポートできます。 コンテナーとメッセージにコピーするには、他のプロバイダーからのエントリは、任意のメッセージの種類を作成するのに使用できるプロバイダーを格納できるように、アドレス帳プロバイダーは、このサポートを提供する必要があります。 他のすべてのサービス ・ プロバイダー向けのオプションです。 名前付きプロパティをサポートしないプロバイダーの MAPI_E_NO_SUPPORT メソッドから返す、 **GetIDsFromNames**と**GetNamesFromIDs**と、**で 0x8000 または大きい値、返される MAPI_E_UNEXPECTED の識別子を持つすべてのプロパティを設定するのには拒否します。SPropProblemarray**。
  
既存またはカスタムのメッセージ クラスの新しいプロパティを定義するのにはクライアントの 1 つの方法は、プロパティの名前を作成します。 サービス プロバイダーは、それぞれのメッセージング システム固有の機能を公開するのに名前付きプロパティを使用できます。 まだ別の名前付きプロパティの使用は、0x8000 未満の識別子を持つプロパティを参照する別の方法を提供します。 
  
などのクライアントでは、すべてのオブジェクトの名前付きプロパティの名前を取得するのに次のコードのようなコードを使用する可能性があります。
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

PS_PUBLIC_STRINGS プロパティのセットからのすべての名前を要求するには、クライアントがプロパティ セットの PS_PUBLIC_STRINGS パラメーターに NULL をとおりに置き換えます。 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a>関連項目

- [MAPI のプロパティの概要](mapi-property-overview.md)


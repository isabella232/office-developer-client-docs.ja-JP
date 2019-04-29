---
title: MAPI ���O�t���v���p�e�B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435048"
---
# <a name="mapi-named-properties"></a>MAPI ���O�t���v���p�e�B
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI には、プロパティに名前を割り当てたり、これらの名前を一意の識別子にマップしたり、このマッピングを永続的にするための機能が用意されています。 id マッピングの永続名を指定すると、プロパティ名はセッション間で有効なままになります。
  
名前付きプロパティを定義するには、クライアントまたはサービスプロバイダーが名前を作成し、それを[mapinameid](mapinameid.md)構造に格納します。 名前は32ビットのグローバル一意識別子 (GUID) と、Unicode 文字列または数値のいずれかで構成されるため、名前付きプロパティの作成者は、重複を恐れることなく、わかりやすい名前を作成できます。 名前は一意であり、識別子の値に関係なく使用できます。 
  
名前付きプロパティをサポートするために、サービスプロバイダーは、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)と[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)の2つのメソッドを実装して、名前と識別子の間を変換し、その[imapiprop:: GetProps](imapiprop-getprops.md) [を許可します。imapiprop:: setprops](imapiprop-setprops.md)メソッドを使用して、名前付きプロパティの範囲内の識別子を持つプロパティを取得および変更します。 名前付きプロパティの識別子の範囲は、0x8000 ~ 0xFFFE です。 
  
**imapiprop**インターフェイスを実装するオブジェクトは、名前付きプロパティをサポートできます。 このサポートを提供するために、他のプロバイダーからのエントリをコンテナーにコピーし、任意のメッセージの種類を作成するために使用できるメッセージストアプロバイダーを使用できるようにするアドレス帳プロバイダー。 他のすべてのサービスプロバイダーのオプションです。 名前付きプロパティをサポートしないプロバイダーは、 **getidsfromnames**および**GetNamesFromIDs**メソッドから MAPI_E_NO_SUPPORT を返し、0x8000 以上**の識別子を持つプロパティを設定することを拒否します。spropの配列**。
  
プロパティの名前を作成することは、クライアントが既存またはカスタムのメッセージクラスの新しいプロパティを定義する1つの方法です。 サービスプロバイダーは、名前付きプロパティを使用して、メッセージングシステムの固有の機能を公開できます。 さらに、名前付きプロパティを使用する別の方法として、0x8000 未満の識別子を持つプロパティを参照する別の方法を提供しています。 
  
たとえば、クライアントは次のようなコードを使用して、オブジェクトのすべての名前付きプロパティの名前を取得することができます。
  
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

PS_PUBLIC_STRINGS プロパティセットからすべての名前を要求する場合、クライアントは次のように、property set パラメーターの NULL を PS_PUBLIC_STRINGS に置き換えます。 
  
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


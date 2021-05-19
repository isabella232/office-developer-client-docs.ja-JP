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
  
MAPI は、プロパティに名前を割り当てる機能、これらの名前を一意の識別子にマッピングし、このマッピングを永続的に行う機能を提供します。 識別子マッピングに対する永続的な名前を使用すると、セッション間でプロパティ名が有効なままになります。
  
名前付きプロパティを定義するには、クライアントまたはサービス プロバイダーが名前を構成し [、MAPINAMEID 構造に格納](mapinameid.md) します。 名前は 32 ビットのグローバル一意識別子 (GUID) と Unicode 文字文字列または数値ででなされるので、名前付きプロパティの作成者は重複を恐れずに意味のある名前を作成できます。 名前は一意であり、識別子の値に関係なく使用できます。 
  
名前付きプロパティをサポートするために、サービス プロバイダーは [、IMAPIProp:::GetIDsFromNames](imapiprop-getidsfromnames.md) と [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) の 2 つのメソッドを実装して、名前と識別子の間で変換し [、IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) メソッドが名前付きプロパティ範囲の識別子を持つプロパティを取得および変更できます。 名前付きプロパティ識別子の範囲は、0x8000と0xFFFE。 
  
**IMAPIProp** インターフェイスを実装するオブジェクトは、名前付きプロパティをサポートできます。 このサポートを提供するには、他のプロバイダーのエントリをコンテナーにコピーできるアドレス帳プロバイダーと、任意のメッセージの種類を作成するために使用できるメッセージ ストア プロバイダーが必要です。 これは、他のすべてのサービス プロバイダーのオプションです。 名前付きプロパティをサポートしていないプロバイダーは **、GetIDsFromNames** メソッドと **GetNamesFromIDs** メソッドから MAPI_E_NO_SUPPORT を返し、0x8000 以上の識別子を持つプロパティの設定を拒否し **、SPropProblemarray** で MAPI_E_UNEXPECTED を返します。
  
プロパティの名前を作成する方法の 1 つは、クライアントが既存のメッセージ クラスまたはカスタム メッセージ クラスの新しいプロパティを定義する方法の 1 つです。 サービス プロバイダーは、名前付きプロパティを使用して、メッセージング システムの一意の機能を公開できます。 名前付きプロパティのもう 1 つの使い方は、以下の識別子を持つプロパティを参照する別の方法を提供0x8000。 
  
たとえば、クライアントは次のようなコードを使用して、オブジェクトのすべての名前付きプロパティの名前を取得できます。
  
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

PS_PUBLIC_STRINGS プロパティ セットからすべての名前を要求するには、クライアントはプロパティ セット パラメーターの NULL を次のようにPS_PUBLIC_STRINGS置き換えます。 
  
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


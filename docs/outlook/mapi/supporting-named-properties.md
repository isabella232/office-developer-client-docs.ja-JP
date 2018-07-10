---
title: 名前付きプロパティをサポートしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 983cbaf4d3523bf1e5370e5ad3119ab8c1490f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804048"
---
# <a name="supporting-named-properties"></a>名前付きプロパティをサポートしています。

  
  
**適用されます**: Outlook 
  
実装する任意のオブジェクト、 [IMAPIProp: IUnknown](imapipropiunknown.md)インターフェイスは、名前付きプロパティをサポートできます。 名前付きプロパティのサポートに必要です。 
  
- アドレス帳プロバイダーのコンテナーにコピーするには、他のプロバイダーからのエントリを許可します。
    
- メッセージは、任意のメッセージの種類を作成するのに使用できるプロバイダーを格納します。
    
名前付きプロパティのサポートは、他のすべてのサービス プロバイダーのオプションです。 名前付きプロパティをサポートしているサービス プロバイダーは、 [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドと[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドの名前の識別子にマッピングを実装しなければなりません。 0x8000 の上の範囲内の 1 つまたは複数のプロパティ識別子に対応する名前を取得する**GetNamesFromIDs**と**GetIDsFromNames**を作成するか、1 つまたは複数の名前の識別子を取得するのには、クライアントが呼び出します。 
  
名前付きプロパティをサポートしていないサービスのプロバイダーにする必要があります。
  
- [SPropProblem](spropproblem.md)配列内の MAPI_E_UNEXPECTED_ID を返すことで 0x8000 以上の識別子を持つプロパティを設定するのには[IMAPIProp::SetProps](imapiprop-setprops.md)への呼び出しは失敗します。 
    
- [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドと[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドから MAPI_E_NO_SUPPORT を返します。 
    

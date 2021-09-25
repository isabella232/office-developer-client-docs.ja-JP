---
title: 名前付きプロパティのサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b989517b38f939796db40291c7a0211c8d3f37fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578544"
---
# <a name="supporting-named-properties"></a>名前付きプロパティのサポート

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
IMAPIProp : [IUnknown](imapipropiunknown.md) インターフェイスを実装するオブジェクトは、名前付きプロパティをサポートできます。 名前付きプロパティのサポートは、次の場合に必要です。 
  
- 他のプロバイダーからのエントリをコンテナーにコピーできるアドレス帳プロバイダー。
    
- 任意のメッセージの種類を作成するために使用できるメッセージ ストア プロバイダー。
    
他のすべてのサービス プロバイダーでは、名前付きプロパティのサポートは省略可能です。 名前付きプロパティをサポートするサービス プロバイダーは [、IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) および [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドに名前と識別子のマッピングを実装する必要があります。 クライアントは **GetNamesFromIDs** を呼び出して、0x8000 以上の範囲の 1 つ以上のプロパティ識別子に対応する名前を取得し **、GetIDsFromNames** を使用して 1 つ以上の名前の識別子を作成または取得します。 
  
名前付きプロパティをサポートしないサービス プロバイダーは、次の必要があります。
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)の呼び出しを失敗して[、SPropProblem](spropproblem.md)配列で 0x8000 以上の識別子を持つプロパティMAPI_E_UNEXPECTED_IDを設定します。 
    
- [IMAPIProp:::GetNamesFromIDs](imapiprop-getnamesfromids.md)および[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドから値を返します。 MAPI_E_NO_SUPPORT 
    


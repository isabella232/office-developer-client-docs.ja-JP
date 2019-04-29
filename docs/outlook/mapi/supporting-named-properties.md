---
title: 名前付きプロパティのサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434327"
---
# <a name="supporting-named-properties"></a>名前付きプロパティのサポート

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[imapiprop: IUnknown](imapipropiunknown.md)インターフェイスを実装するオブジェクトは、名前付きプロパティをサポートできます。 名前付きプロパティのサポートは、次の場合に必要です。 
  
- 他のプロバイダーからのエントリをコンテナーにコピーできるアドレス帳プロバイダー。
    
- 任意のメッセージの種類を作成するために使用できるメッセージストアプロバイダー。
    
名前付きプロパティのサポートは、他のすべてのサービスプロバイダーでは省略可能です。 名前付きプロパティをサポートするサービスプロバイダーは、 [imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)および[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドに名前から識別子へのマッピングを実装する必要があります。 クライアントは**GetNamesFromIDs**を呼び出して、1つ以上の名前の識別子を作成または取得するために、0x8000 を超える範囲および**getidsfromnames**内の1つ以上のプロパティ識別子に対応する名前を取得します。 
  
名前付きプロパティをサポートしていないサービスプロバイダーは次のようにする必要があります。
  
- 失敗した[imapiprop:: setprops](imapiprop-setprops.md)を使用して、id 0x8000 以上のプロパティを設定します。この値は、 [spropproblem](spropproblem.md)の配列の MAPI_E_UNEXPECTED_ID を返します。 
    
- [imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)および[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドから MAPI_E_NO_SUPPORT を返します。 
    


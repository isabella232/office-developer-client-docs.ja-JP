---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: 必要な同期タスクを決定するために Outlook で使用するトランスポート設定を表し、アカウントがサポートしていないユーザーインターフェイス (UI) 要素を無効にします。
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404527"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

必要な同期タスクを決定するために Outlook で使用するトランスポート設定を表し、アカウントがサポートしていないユーザーインターフェイス (UI) 要素を無効にします。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x2010  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティタグ:  <br/> |0x20100102  <br/> |
|接続  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount:: getprop](iolkaccount-getprop.md)または[IOlkAccount:: setprop](iolkaccount-setprop.md)を使用して、このプロパティを取得または設定します。
  
アカウントがメッセージを送信するだけでメッセージを受信できない場合は、 **MAPIACCT_SEND_ONLY**を返します。 この場合、Outlook では、この種類のアカウントに適用されない ui (たとえば、**送信/受信**の ui) を無効にします。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)


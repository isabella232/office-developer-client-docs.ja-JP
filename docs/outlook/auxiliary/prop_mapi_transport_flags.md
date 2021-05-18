---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: 必要な同期タスクOutlook、アカウントがサポートしていないユーザー インターフェイス (UI) 要素を無効にするために使用するトランスポート設定を表します。
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404527"
---
# <a name="prop_mapi_transport_flags"></a>PROP_MAPI_TRANSPORT_FLAGS

必要な同期タスクOutlook、アカウントがサポートしていないユーザー インターフェイス (UI) 要素を無効にするために使用するトランスポート設定を表します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x2010  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ:  <br/> |0x20100102  <br/> |
|アクセス:  <br/> |読み取り/書き込み  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp](iolkaccount-getprop.md)または[IOlkAccount::SetProp](iolkaccount-setprop.md)をそれぞれ使用して、このプロパティを取得または設定します。
  
アカウントが **MAPIACCT_SEND_ONLY** のみ送信できますが、メッセージを受信できない場合は、この値を返します。 この場合、Outlook種類のアカウント (たとえば、送信/受信の UI) に適用されない UI が **無効にされます**。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)


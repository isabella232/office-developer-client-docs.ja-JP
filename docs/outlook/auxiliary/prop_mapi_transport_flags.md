---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Outlook を使用して必要な同期タスクを決定し、アカウントをサポートしないユーザー インターフェイス (UI) 要素を無効にするトランスポートの設定を表します。
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799569"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

Outlook を使用して必要な同期タスクを決定し、アカウントをサポートしないユーザー インターフェイス (UI) 要素を無効にするトランスポートの設定を表します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x2010  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ。  <br/> |0x20100102  <br/> |
|アクセス:  <br/> |値の取得および設定が可能です。  <br/> |
   
## <a name="remarks"></a>備考

取得または[IOlkAccount::GetProp](iolkaccount-getprop.md)または[IOlkAccount::SetProp](iolkaccount-setprop.md)をそれぞれ使用して、このプロパティを設定します。
  
アカウントは、メッセージの送信だけが、メッセージを受信できない場合は、 **MAPIACCT_SEND_ONLY**を返します。 この例では、Outlook には、この種類のアカウント (**送信/受信**するための UI など) には適用されない UI が無効になります。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)


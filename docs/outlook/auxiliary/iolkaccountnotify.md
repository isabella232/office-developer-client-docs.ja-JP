---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: ab24feca84e7049a9800b860c332db52d19cf929
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412500"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

アカウントに対する変更のコールバックをクライアントに提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|提供元:  <br/> | クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[Notify](iolkaccountnotify-notify.md) <br/> |指定したアカウントへの変更をクライアントに通知します。  <br/> |
   
## <a name="remarks"></a>注釈

このインターフェイスは、通知の設定時 [に IOlkAccountManager::Advise](iolkaccountmanager-advise.md) に渡されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


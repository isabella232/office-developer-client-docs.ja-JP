---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: 1d9b659cee551140aedd4caf21d929f6df2bfc72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605387"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

アカウントに対する変更のコールバックをクライアントに提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|提供元:  <br/> | Client  <br/> |
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


---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: f4b57ad1062df9aa1809e8eb422a2c983adcac4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799488"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

アカウントへの変更をクライアントにコールバックを提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承します。  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|提供元:  <br/> | クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[Notify](iolkaccountnotify-notify.md) <br/> |指定したアカウントへの変更がクライアントに通知します。  <br/> |
   
## <a name="remarks"></a>備考

このインターフェイスは、通知を設定するときに、 [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)に渡されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


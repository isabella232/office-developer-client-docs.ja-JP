---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: ab24feca84e7049a9800b860c332db52d19cf929
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322072"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

アカウントの変更についてクライアントへのコールバックを提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|提供元:  <br/> | クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[Notify](iolkaccountnotify-notify.md) <br/> |指定したアカウントへの変更をクライアントに通知します。  <br/> |
   
## <a name="remarks"></a>解説

このインターフェイスは、通知を設定するときに[IOlkAccountManager:: アドバイズ](iolkaccountmanager-advise.md)に渡されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


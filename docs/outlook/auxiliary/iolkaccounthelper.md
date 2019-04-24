---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322156"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

現在の MAPI セッションでアカウントを管理するためのヘルパー機能を提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|提供元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[Placeholder1](iolkaccounthelper-placeholder1.md) <br/> | *このメンバーはプレースホルダーで、サポートされていません。*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |アカウントのプロファイル名を取得します。  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |MAPI セッションを開き、アカウントマネージャーのセッションへの参照を保持します。  <br/> |
|[「sosoffsession」](iolkaccounthelper-handsoffsession.md) <br/> |[IOlkAccountHelper:: GetMapiSession](iolkaccounthelper-getmapisession.md)によって返された MAPI セッションオブジェクトを解放します。  <br/> |
   
## <a name="remarks"></a>解説

このインターフェイスは、アカウントマネージャーを初期化するときに[IOlkAccountManager:: Init](iolkaccountmanager-init.md)に渡されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


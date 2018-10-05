---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386412"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

アカウントを管理する現在の MAPI セッションでは、ヘルパー機能を提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承します。  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|提供元:  <br/> |クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[Placeholder1](iolkaccounthelper-placeholder1.md) <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |アカウントのプロファイル名を取得します。  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |MAPI セッションを開くし、アカウント マネージャーのセッションへの参照を保持します。  <br/> |
|[HandsOffSession](iolkaccounthelper-handsoffsession.md) <br/> |[IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)によって返された MAPI セッション オブジェクトを解放します。  <br/> |
   
## <a name="remarks"></a>備考

このインターフェイスは、アカウント マネージャーを初期化するときに、 [IOlkAccountManager::Init](iolkaccountmanager-init.md)に渡されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


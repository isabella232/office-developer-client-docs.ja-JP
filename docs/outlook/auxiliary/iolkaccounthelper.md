---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 3c28b1e8ab7e2d72d27cc6545b6ef57834ef5b6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799457"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

アカウントを管理する現在の MAPI セッションでは、ヘルパー機能を提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承します。  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|提供元:  <br/> |クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[Placeholder1](iolkaccounthelper-placeholder1.md) <br/> | *このメンバーは、プレース ホルダーではサポートされていません。*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |アカウントのプロファイル名を取得します。  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |MAPI セッションを開くし、アカウント マネージャーのセッションへの参照を保持します。  <br/> |
|[HandsOffSession](iolkaccounthelper-handsoffsession.md) <br/> |[IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)によって返された MAPI セッション オブジェクトを解放します。  <br/> |
   
## <a name="remarks"></a>注釈

このインターフェイスは、アカウント マネージャーを初期化するときに、 [IOlkAccountManager::Init](iolkaccountmanager-init.md)に渡されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


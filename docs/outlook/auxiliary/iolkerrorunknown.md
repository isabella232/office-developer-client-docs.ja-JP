---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: dc2fe6bbaf4515d5c5f5be694b15040bf03ef374
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321855"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

最新のエラーについての詳細情報を提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|提供元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |指定したエラーのメッセージ文字列を取得します。  <br/> |
   
## <a name="remarks"></a>解説

このインターフェイスは、 [IOlkAccountManager](iolkaccountmanager.md)、 [IOlkAccountNotify](iolkaccountnotify.md)、および[IOlkAccount](iolkaccount.md)のエラーに関するその他の情報を提供します。 また、 **IOlkAccountManager**、 **IOlkAccountNotify**、および**IOlkAccount**の基本インターフェイスでもあります。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)


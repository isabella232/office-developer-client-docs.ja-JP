---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389737"
---
# <a name="iolkenum"></a>IOlkEnum

[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown)オブジェクトとしてアカウントの列挙をサポートします。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承します。  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|実装元:  <br/> |Outlook  <br/> |
|提供元:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |列挙子では、アカウントの数を取得します。  <br/> |
|[Reset](iolkenum-reset.md) <br/> |先頭に列挙子をリセットします。  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |列挙子では、次のアカウントを取得します。  <br/> |
|[スキップ](iolkenum-skip.md) <br/> |列挙子内のアカウントの指定した数をスキップします。  <br/> |
   
## <a name="remarks"></a>備考

アカウントの列挙子を取得するときは、 **IOlkAccountManager::EnumerateAccounts**によってこのインターフェイスが返されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


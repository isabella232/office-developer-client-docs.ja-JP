---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 19ec67bf033859073e7685912196369b664f4a36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592690"
---
# <a name="iolkenum"></a>IOlkEnum

[IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown)オブジェクトとしてアカウントの列挙をサポートします。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承します。  <br/> |[IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
|提供元:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |列挙子では、アカウントの数を取得します。  <br/> |
|[Reset](iolkenum-reset.md) <br/> |先頭に列挙子をリセットします。  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |列挙子では、次のアカウントを取得します。  <br/> |
|[スキップ](iolkenum-skip.md) <br/> |列挙子内のアカウントの指定した数をスキップします。  <br/> |
   
## <a name="remarks"></a>注釈

アカウントの列挙子を取得するときは、 **IOlkAccountManager::EnumerateAccounts**によってこのインターフェイスが返されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


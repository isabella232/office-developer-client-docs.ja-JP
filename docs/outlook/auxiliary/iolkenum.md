---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322100"
---
# <a name="iolkenum"></a>IOlkEnum

[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown)オブジェクトとしてのアカウントの列挙をサポートします。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|実装元:  <br/> |Outlook  <br/> |
|提供元:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |列挙子内のアカウントの数を取得します。  <br/> |
|[Reset](iolkenum-reset.md) <br/> |列挙子を最初にリセットします。  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |列挙子の次のアカウントを取得します。  <br/> |
|[Skip](iolkenum-skip.md) <br/> |列挙子内の指定された数のアカウントをスキップします。  <br/> |
   
## <a name="remarks"></a>解説

このインターフェイスは、アカウントの列挙子を取得するときに、 **IOlkAccountManager:: EnumerateAccounts**によって返されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: e18d23847744425bd7feb62dd615a4dcfa1c9287
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625645"
---
# <a name="iolkenum"></a>IOlkEnum

[IUnknown オブジェクトとしてアカウントの列挙をサポート](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown)します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|実装元:  <br/> |Outlook  <br/> |
|提供元:  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |列挙子内のアカウントの数を取得します。  <br/> |
|[Reset](iolkenum-reset.md) <br/> |列挙子を先頭にリセットします。  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |列挙子の次のアカウントを取得します。  <br/> |
|[Skip](iolkenum-skip.md) <br/> |列挙子内の指定した数のアカウントをスキップします。  <br/> |
   
## <a name="remarks"></a>注釈

このインターフェイスは、アカウントの列挙子を取得するときに **、IOlkAccountManager::EnumerateAccounts** によって返されます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799503"
---
# <a name="iolkenum"></a>IOlkEnum

[IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx)オブジェクトとしてアカウントの列挙をサポートします。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承します。  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
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


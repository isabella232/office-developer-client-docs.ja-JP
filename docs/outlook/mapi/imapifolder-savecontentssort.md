---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411618"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの contents テーブルの既定の並べ替え順序を設定します。
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpsortcriteria_
  
> 順番既定の並べ替え順序を含む[ssortorderset](ssortorderset.md)構造体へのポインター。 
    
 _ulFlags_
  
> 順番既定の並べ替え順序を設定する方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
RECURSIVE_SORT 
  
> 既定の並べ替え順序セットは、指定したフォルダーとそのすべてのサブフォルダーに適用されます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 並べ替え順序が正常に保存されました。
    
MAPI_E_NO_SUPPORT 
  
> メッセージストアプロバイダーは、フォルダーコンテンツテーブルの並べ替え順序の保存をサポートしていません。
    
## <a name="remarks"></a>注釈

**imapifolder:: SaveContentsSort**メソッドは、フォルダーの contents テーブルに既定の並べ替え順序を設定します。 つまり、クライアントが**SaveContentsSort**を呼び出した後に、フォルダーの[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを呼び出すと、返されたコンテンツテーブルの行が**SaveContentsSort**で設定された順序で表示されます。
  
すべてのメッセージストアプロバイダーが**SaveContentsSort**をサポートしているわけではありません。メッセージストアプロバイダーは、 **SaveContentsSort**メソッドから MAPI_E_NO_SUPPORT を返すことができます。 
  
## <a name="see-also"></a>関連項目



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


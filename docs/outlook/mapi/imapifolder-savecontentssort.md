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
  
フォルダーのコンテンツ テーブルの既定の並べ替え順序を設定します。
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpSortCriteria_
  
> [in]既定の並べ替え順序を含む [SSortOrderSet](ssortorderset.md) 構造体へのポインター。 
    
 _ulFlags_
  
> [in]既定の並べ替え順序の設定方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
RECURSIVE_SORT 
  
> 既定の並べ替え順序セットは、指定されたフォルダーとそのすべてのサブフォルダーに適用されます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 並べ替え順序が正常に保存されました。
    
MAPI_E_NO_SUPPORT 
  
> メッセージ ストア プロバイダーは、フォルダーコンテンツ テーブルの並べ替え順序の保存をサポートされていません。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::SaveContentsSort** メソッドは、フォルダーのコンテンツ テーブルの既定の並べ替え順序を確立します。 つまり、コードが **SaveContentsSort** を呼び出した後にクライアントがフォルダーの [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出す場合、返されるコンテンツ テーブルの行は **SaveContentsSort** によって確立された順序で表示されます。
  
すべてのメッセージ ストア プロバイダーが **SaveContentsSort をサポートしているのではありません**。メッセージ ストア プロバイダーが **SaveContentsSort** メソッドからMAPI_E_NO_SUPPORTを返すのは許容されます。 
  
## <a name="see-also"></a>関連項目



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


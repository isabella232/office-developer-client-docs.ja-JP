---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1e16f14afda35ec67375f77371f7601f056e968f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596331"
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


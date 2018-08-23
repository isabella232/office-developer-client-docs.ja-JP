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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1f79265c4356747e64aa8102dd4486db229baf5a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579663"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォルダーの内容のテーブルの既定の並べ替え順序を設定します。
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpSortCriteria_
  
> [in]既定の並べ替え順序を含む[SSortOrderSet](ssortorderset.md)構造体へのポインター。 
    
 _ulFlags_
  
> [in]既定の並べ替え順序を設定する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
RECURSIVE_SORT 
  
> 既定の並べ替え順序を設定は、指定されたフォルダーとそのすべてのサブフォルダーに適用されます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 並べ替え順序が正しく保存されました。
    
MAPI_E_NO_SUPPORT 
  
> メッセージ ストア プロバイダーでは、そのフォルダーの内容のテーブルの並べ替え順序を保存することはできません。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::SaveContentsSort**メソッドは、フォルダーの内容のテーブルの既定の並べ替え順序を確立します。 **SaveContentsSort**コードの呼び出しの後、クライアントがフォルダーの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出すと、返されるコンテンツ テーブル内の行は**SaveContentsSort**によって確立された順序で表示されます。
  
すべてのメッセージ ストア プロバイダーをサポートして**SaveContentsSort**。メッセージ ストア プロバイダーは、 **SaveContentsSort**メソッドから MAPI_E_NO_SUPPORT を返すことができます。 
  
## <a name="see-also"></a>関連項目



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


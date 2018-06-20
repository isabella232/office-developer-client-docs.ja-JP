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
ms.openlocfilehash: 7c8ccada96b3e34372d488e16c85627e8b6b0cd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800492"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**適用されます**: Outlook 
  
フォルダーの内容のテーブルの既定の並べ替え順序を設定します。
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

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
    
## <a name="remarks"></a>備考

**IMAPIFolder::SaveContentsSort**メソッドは、フォルダーの内容のテーブルの既定の並べ替え順序を確立します。 **SaveContentsSort**コードの呼び出しの後、クライアントがフォルダーの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出すと、返されるコンテンツ テーブル内の行は**SaveContentsSort**によって確立された順序で表示されます。
  
すべてのメッセージ ストア プロバイダーをサポートして**SaveContentsSort**。メッセージ ストア プロバイダーは、 **SaveContentsSort**メソッドから MAPI_E_NO_SUPPORT を返すことができます。 
  
## <a name="see-also"></a>関連項目



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)


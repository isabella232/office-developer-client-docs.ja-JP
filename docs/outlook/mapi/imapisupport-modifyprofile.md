---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 98e6331d5a9e52d5ae73ed12d8c045bdf226c2c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800750"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**適用されます**: Outlook 
  
永続的なプロファイルのセクションを保存するメッセージを変更します。
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]メッセージの種類を示すフラグのビットマスクを格納します。 次のフラグを設定することができます。
    
MDB_TEMPORARY 
  
> メッセージ ・ ストアでは、一時的なものと、メッセージ ストアのテーブルに追加できませんする必要があります。 MDB_TEMPORARY を設定すると、 **ModifyProfile**はすぐに S_OK を返します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロファイル セクションへの変更は成功しました。
    
## <a name="remarks"></a>備考

メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::ModifyProfile**メソッドを実装します。 メッセージのストア プロバイダーの呼び出し**ModifyProfile**プロファイル情報を変更するのには MAPI メッセージを表示します。 
  
 **ModifyProfile**は、インストールされているメッセージ ストア プロバイダーのリソースの一覧を呼び出し元のプロバイダーに関連付けられているプロファイルのセクションを追加します。 [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)メソッドを介してクライアントには、メッセージ ストアのテーブルに登録して、ダイアログ ボックスの表示を開くには、メッセージ ストアが発生します。 
  
MDB_TEMPORARY フラグが設定されている場合、MAPI は何し、メソッドは、すぐに S_OK を返します。
  
## <a name="see-also"></a>関連項目



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


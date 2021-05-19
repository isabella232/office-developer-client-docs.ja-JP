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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419990"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア のプロファイル セクションを永続的に変更します。
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]メッセージ ストアの種類を示すフラグのビットマスク。 次のフラグを設定できます。
    
MDB_TEMPORARY 
  
> メッセージ ストアは一時的なもので、メッセージ ストア テーブルに追加する必要があります。 このMDB_TEMPORARY設定すると **、ModifyProfile は** 直ちにS_OK返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイル セクションの変更が成功しました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::ModifyProfile** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 メッセージ ストア プロバイダーは **ModifyProfile を呼び出** して、MAPI にプロファイル情報の変更を求めるプロンプトを表示します。 
  
 **ModifyProfile は** 、呼び出し元プロバイダーに関連付けられているプロファイル セクションを、インストールされているメッセージ ストア プロバイダー リソースの一覧に追加します。 これにより [、IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) メソッドを使用してクライアントが使用できるメッセージ ストア テーブルにメッセージ ストアが一覧表示され、ダイアログ ボックスが表示されることなく開きます。 
  
このフラグMDB_TEMPORARY設定されている場合、MAPI は何も実行しません。メソッドは、このフラグを使用してすぐにS_OK。
  
## <a name="see-also"></a>関連項目



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


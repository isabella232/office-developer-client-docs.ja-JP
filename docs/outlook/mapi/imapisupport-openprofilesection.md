---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cf4f3954b529dd40fe3b273f0bc469766645da33
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592390"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のプロファイルのセクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>パラメーター

 _lpUid_
  
> [in]開くプロファイル [セクションを識別する MAPIUID](mapiuid.md) 構造体へのポインター。 _lpUid_ パラメーターに NULL を渡すと、呼び出し元のプロファイル セクションが開きます。 
    
 _ulFlags_
  
> [in]プロファイル セクションの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> **OpenProfileSection は**、プロファイル セクションが呼び出し元から完全にアクセスできる前に、正常に戻ります。 プロファイル セクションにアクセスできない場合は、後続のオブジェクト呼び出しを実行すると、エラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用として開かれません。呼び出し元は、読み取り/書き込みアクセス許可が付与されているという前提では動作しません。 
    
 _lppProfileObj_
  
> [out]開いたプロファイル セクションへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイル セクションが正常に開かされました。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用のプロファイル セクションを変更しようとしたり、呼び出し元が不十分なアクセス許可を持つオブジェクトにアクセスしようとしたりしました。
    
MAPI_E_NOT_FOUND 
  
> lpEntryID で渡されたエントリ識別子に関連付  _けられたプロファイル セクションは含めではありません_。
    
MAPI_E_UNKNOWN_FLAGS 
  
> 予約済みまたはサポートされていないフラグが使用されたため、操作は完了しなかった。
    
## <a name="remarks"></a>注釈

**IMAPISupport::OpenProfileSection** メソッドは、すべてのサポート オブジェクトに実装されます。 サービス プロバイダーとメッセージ サービスは **、OpenProfileSection** を呼び出してプロファイル セクションを開き、 **その IProfSect** インターフェイス実装へのポインターを取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **OpenProfileSection** は  _、ulFlags_ パラメーターで MAPI_MODIFY フラグを設定し、アクセス許可が十分でない限り、プロファイル セクションを読み取り専用として開きます。 このフラグを設定しても、読み取り/書き込みアクセス許可は保証されない。付与されるアクセス許可は、アクセス レベルとオブジェクトによって異なる。 
  
**OpenProfileSection** が存在しないプロファイル セクションを読み取り専用として開くことを試みる場合、そのセクションはMAPI_E_NOT_FOUND。 **OpenProfileSection** が存在しないプロファイル セクションを読み取り/書き込みとして開く場合は、プロファイル セクションを作成し **、IProfSect** ポインターを返します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


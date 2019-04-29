---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411387"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のプロファイルのセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>パラメーター

 _lpuid_
  
> 順番開くプロファイルセクションを識別する[MAPIUID](mapiuid.md)構造体へのポインター。 _lpuid_パラメーターに NULL を渡すと、呼び出し元のプロファイルセクションが開きます。 
    
 _ulFlags_
  
> 順番プロファイルセクションが開かれる方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し**** 元がプロファイルセクションに完全にアクセスできるようになる前に、openプロファイルを正常に返すことができるようにします。 プロファイルセクションにアクセスできない場合は、次のオブジェクト呼び出しを行うとエラーが発生することがあります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用として開かれ、読み取り/書き込みアクセス許可が付与されているという前提で呼び出し元は機能しません。 
    
 _lppprofileobj_
  
> 読み上げ開いているプロファイルセクションへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルセクションが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用プロファイルセクションを変更しようとしたか、呼び出し元が十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。
    
MAPI_E_NOT_FOUND 
  
> _lな tryid_で渡されるエントリ識別子に関連付けられているプロファイルセクションはありません。
    
MAPI_E_UNKNOWN_FLAGS 
  
> 予約済みまたは未サポートのフラグが使用されたため、操作が完了しませんでした。
    
## <a name="remarks"></a>注釈

**imapisupport:: openプロファイル**のメソッドは、すべてのサポートオブジェクトに実装されています。 サービスプロバイダおよびメッセージサービスは**** 、openprofile を呼び出して、プロファイルセクションを開き、その**IProfSect**インターフェイス実装へのポインターを取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **openprofile**の場合は、MAPI_MODIFY フラグを_ulflags_パラメーターに設定し、アクセス許可で十分でなければ、プロファイルセクションを読み取り専用として開きます。 このフラグを設定しても、読み取り/書き込みアクセス許可は保証されません。付与されるアクセス許可は、アクセスレベルとオブジェクトによって異なります。 
  
**openprofile**が、存在しないプロファイルセクションを読み取り専用として開こうとした場合は、MAPI_E_NOT_FOUND を返します。 **openprofile**が、存在しないプロファイルセクションを読み取り/書き込みとして開こうとした場合、プロファイルセクションを作成し、 **IProfSect**ポインターを返します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


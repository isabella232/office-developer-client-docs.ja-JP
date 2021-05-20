---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439920"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のプロファイルのセクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>パラメーター

 _lpUID_
  
> [in]プロファイル セクションを識別 [する MAPIUID](mapiuid.md) 構造体へのポインター。 
    
 _lpInterface_
  
> [in]プロファイル セクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合  _、lppProfSect_ パラメーターはプロファイル セクションの標準インターフェイス **IProfSect へのポインターを返します**。
    
 _ulFlags_
  
> [in]プロファイル セクションへのアクセスを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> プロファイル セクションが呼び出し元のクライアントで完全に使用できる前に **、OpenProfileSection** が正常に返されるのを許可します。 プロファイル セクションを使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。 
    
MAPI_FORCE_ACCESS
  
> プロバイダーに属していないプロファイル セクションへのアクセスを許可します。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、プロファイル セクションは読み取り専用のアクセス許可で開かれません。クライアントは、読み取り/書き込みアクセス許可が付与されているという前提で動作しません。 
    
 _lppProfSect_
  
> [out]プロファイル セクションへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイル セクションが正常に開かされました。
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元のアクセス許可が不十分なプロファイル セクションへのアクセスが試行されました。
    
MAPI_E_NOT_FOUND 
  
> 要求されたプロファイル セクションが存在しません。
    
## <a name="remarks"></a>注釈

**IMAPISession::OpenProfileSection** メソッドは **、IProfSect** インターフェイスをサポートするプロファイル セクションまたはオブジェクトを開きます。 プロファイル セクションは、セッション プロファイルからの情報の読み取りおよびセッション プロファイルへの書き込みに使用されます。 
  
**OpenProfileSection** を使用して _、ulFlags_ パラメーターでユーザー名を指定しない限り、個々のサービス プロバイダーが所有するプロファイル セクションMAPI_FORCE_ACCESS開くことができません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数のクライアントが読み取り専用アクセス許可を持つプロファイル セクションを開くことができますが、読み取り/書き込みアクセス許可を持つプロファイル セクションを開くことができるのは 1 つのクライアントのみです。 MAPI_MODIFY フラグを設定して **OpenProfileSection** を呼び出して開くプロファイル セクションが別のクライアントにある場合、呼び出しは失敗し、MAPI_E_NO_ACCESS。 
  
セクションが書き込み用に開いている場合、読み取り専用の開く操作は失敗します。 
  
プロファイル セクションを作成するには **、openProfileSection** を呼び出して、MAPI_MODIFY フラグと _lpUID_ パラメーターに存在しない **MAPIUID** 構造を指定します。 必ずユーザー設定を指定MAPI_MODIFY。 存在しない _MAPIUID_ をポイントする lpUIDを設定し **、OpenProfileSection** が読み取り専用の既定のアクセス モードを使用するために設定されている場合、呼び出しは MAPI_E_NOT_FOUND で失敗します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


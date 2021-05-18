---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405661"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のプロファイルからプロファイル セクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。 
  
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
  
> [in]開くプロファイル セクションの一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。 クライアントは、lpUID パラメーターに  _NULL を渡す必要_ があります。 サービス プロバイダーは、メッセージ サービスエントリ ポイント関数から呼び出す **際に、MAPIUID** を取得するために NULL を渡します。 
    
 _lpInterface_
  
> [in]プロファイル セクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合、プロファイル セクションの標準インターフェイス (**IProfSect**) が返されます。 
    
 _ulFlags_
  
> [in]プロファイル セクションの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> **OpenProfileSection を** 有効にし、プロファイル セクションが呼び出し元で完全に使用できる前に、正常に戻ります。 プロファイル セクションが使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、オブジェクトは読み取り専用のアクセス許可で開かれません。呼び出し元は、読み取り/書き込みアクセス許可が付与されているという前提では動作しません。 クライアントは、プロファイルのプロバイダー セクションに対する読み取り/書き込みアクセス許可を許可されません。
    
MAPI_FORCE_ACCESS
  
> 個々のサービス プロバイダーが所有するプロファイル セクションにもアクセスできます。
    
 _lppProfSect_
  
> [out]プロファイル セクションへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイル セクションが正常に開かされました。
    
MAPI_E_NO_ACCESS 
  
> 読み取り専用のプロファイル セクションを変更しようとしたり、ユーザーのアクセス許可が不十分なオブジェクトにアクセスしようとしたりしました。
    
MAPI_E_NOT_FOUND 
  
> 要求されたプロファイル セクションが存在しません。
    
## <a name="remarks"></a>注釈

**IProviderAdmin::OpenProfileSection** メソッドは、プロファイル セクションを開き、呼び出し元がアクティブ なプロファイルから情報を読み取り、情報を書き込む可能性があります。 
  
**クライアントは、OpenProfileSection** メソッドを使用してプロバイダーに属するプロファイル セクションを開くことができません。 
  
複数のクライアントまたはサービス プロバイダーは、読み取り専用アクセス許可を持つプロファイル セクションを同時に開くことができます。 ただし、プロファイル セクションが読み取り/書き込みアクセス許可で開いている場合、アクセスの種類に関係なく、セクションを開く他の呼び出しを行う必要はありません。 プロファイル セクションが読み取り専用アクセス許可で開いている場合、読み取り/書き込みアクセス許可を要求する後続の呼び出しは、MAPI_E_NO_ACCESS。 同様に、セクションが読み取り/書き込みアクセス許可で開いている場合、読み取り専用のアクセス許可を要求する後続の呼び出しも失敗します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**OpenProfileSection** に _ulFlags_ で MAPI_MODIFY を渡し、lpUID で不明な **MAPIUID** を渡して存在しないプロファイル セクションを開くことを要求すると、プロファイル セクションが作成されます。 
  
**OpenProfileSection が読み取** り専用のアクセス許可を持つ存在しないセクションを開くことを要求した場合は、そのセクションがMAPI_E_NOT_FOUND。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI は **、IProviderAdmin::OpenProfileSection** メソッドを使用して、現在のプロファイルからプロファイル セクションを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)


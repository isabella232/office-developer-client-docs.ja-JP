---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437113"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
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
  
> プロファイル セクションを識別 [する MAPIUID](mapiuid.md) 構造体へのポインター。 
    
 _lpInterface_
  
> [in]プロファイル セクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合、標準インターフェイスへのポインターが  _lppProfSect パラメーターで返_ されます。 プロファイル セクションの標準インターフェイスは **IProfSect です**。
    
 _ulFlags_
  
> [in]プロファイル セクションへのアクセスを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> プロファイル セクションが呼び出し元のクライアントで完全に使用できる前に **、OpenProfileSection** が正常に返されるのを許可します。 プロファイル セクションが使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、プロファイル セクションは読み取り専用のアクセス許可で開かれません。クライアントは、読み取り/書き込みアクセス許可が付与されているという前提で動作しません。 
    
MAPI_FORCE_ACCESS
  
> 個々のサービス プロバイダーが所有するプロファイル セクションにもアクセスできます。
    
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

**IMsgServiceAdmin::OpenProfileSection** メソッドは [、IProfSect](iprofsectimapiprop.md)インターフェイスをサポートするオブジェクトであるプロファイル セクションを開きます。 プロファイル セクションは、セッション プロファイルからの情報の読み取りおよびセッション プロファイルへの書き込みに使用されます。 
  
 **OpenProfileSection** を使用して、個々のサービス プロバイダーが所有するプロファイル セクションを開MAPI_FORCE_ACCESS使用できません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数のクライアントが読み取り専用アクセス許可を持つプロファイル セクションを開くことができますが、読み取り/書き込みアクセス許可を持つプロファイル セクションを開くことができるのは 1 つのクライアントのみです。 MAPI_MODIFY フラグを設定して **OpenProfileSection** を呼び出して開くプロファイル セクションが別のクライアントにある場合、呼び出しは失敗し、MAPI_E_NO_ACCESS。 
  
セクションが書き込み用に開いている場合、読み取り専用の開く操作は失敗します。 
  
プロファイル セクションを作成するには **、openProfileSection** を呼び出して、MAPI_MODIFY フラグと _lpUID_ パラメーターに存在しない [MAPIUID](mapiuid.md)構造を指定します。 必ず指定する必要MAPI_MODIFY。 存在しない _MAPIUID_ をポイントする lpUIDを設定し **、OpenProfileSection** が読み取り専用の既定のアクセス モードを使用するために設定されている場合、呼び出しは MAPI_E_NOT_FOUND で失敗します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI は **、IMsgServiceAdmin::OpenProfileSection** メソッドを使用してプロファイル セクションを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)


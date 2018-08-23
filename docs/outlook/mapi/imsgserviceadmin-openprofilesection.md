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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8dfa777480af48819e5357fad9b1e7524148a8b7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568813"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
現在のプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。 
  
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
  
> プロファイル セクションを識別する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _lpInterface_
  
> [in]プロファイル セクションにアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _LppProfSect_パラメーターで返される、標準のインターフェイスへのポインターに NULL を渡すことが発生します。 プロファイル セクションのための標準インターフェイスは、 **IProfSect**です。
    
 _ulFlags_
  
> [in]プロファイル セクションへのアクセスを制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DEFERRED_ERRORS 
  
> 正常に完了するのには**OpenProfileSection**では、可能性のあるプロファイルする前にセクションは、呼び出し側のクライアントに完全に使用可能。 プロファイル セクションが利用できない場合は、それ以降の呼び出しを行うとエラーが発生します。 
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、読み取り専用のアクセス許可を持つプロファイルのセクションを開くし、クライアントが読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。 
    
MAPI_FORCE_ACCESS
  
> 個々 のサービス ・ プロバイダーが所有するものであっても、すべてのプロファイル セクションへのアクセスを許可します。
    
 _lppProfSect_
  
> [out]プロファイル セクションへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロファイル セクションが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元が十分なアクセス許可を持っているプロファイル セクションにアクセスしようとしました。
    
MAPI_E_NOT_FOUND 
  
> 要求したプロファイル セクションが存在しません。
    
## <a name="remarks"></a>注釈

**IMsgServiceAdmin::OpenProfileSection**メソッドは、プロファイルのセクションでは、 [IProfSect](iprofsectimapiprop.md)インターフェイスをサポートするオブジェクトを開きます。 プロファイルのセクションでは、情報の読み込みおよびセッション ・ プロファイル情報を書き込むのために使用されます。 
  
 **OpenProfileSection**は、MAPI_FORCE_ACCESS を使用しない場合は、個々 のサービス ・ プロバイダーが所有するプロファイルのセクションを開くには使用できません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数のクライアントが読み取り専用のアクセス許可を持つプロファイル セクションを開くことができますが、1 つのクライアントは、読み取り/書き込みアクセス許可を持つプロファイル セクションを開くことができます。 プロファイルのセクションを開くには、MAPI_MODIFY フラグを設定して**OpenProfileSection**を呼び出すことで開こうとすると、別のクライアントの場合は、MAPI_E_NO_ACCESS を返す呼び出しが失敗します。 
  
セクションが書き込み用に開いている場合、読み取り専用ファイルを開く操作が失敗します。 
  
MAPI_MODIFY フラグと、 _lpUID_パラメーターに存在しない[MAPIUID](mapiuid.md)構造体の**OpenProfileSection**を呼び出すことによって、プロファイルのセクションを作成できます。 MAPI_MODIFY を指定することを確認します。 存在しない**MAPIUID**を指すように_lpUID_を設定すると、 **OpenProfileSection**は読み取り専用の既定のアクセス モードを使用する設定は、MAPI_E_NOT_FOUND の呼び出しは失敗します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI では、 **IMsgServiceAdmin::OpenProfileSection**メソッドを使用して、プロファイルのセクションを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)


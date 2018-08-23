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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e5f329ef0d3483683d5c94ed38c6631d86e77b93
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800706"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**適用対象**: Outlook 
  
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
  
> [in]プロファイル セクションを識別する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _lpInterface_
  
> [in]プロファイル セクションにアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 プロファイル セクションの標準的なインターフェイス、 **IProfSect**へのポインターを返すに_lppProfSect_パラメーターは、NULL を渡すことです。
    
 _ulFlags_
  
> [in]プロファイル セクションへのアクセスを制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DEFERRED_ERRORS 
  
> 正常に完了するのには**OpenProfileSection**では、可能性のあるプロファイルする前にセクションは、呼び出し側のクライアントに完全に使用可能。 プロファイル セクションが利用できない場合は、それ以降の呼び出しを行うとエラーが発生することができます。 
    
MAPI_FORCE_ACCESS
  
> プロバイダーに属していないプロファイル セクションへのアクセスを許可します。
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、読み取り専用のアクセス許可を持つプロファイルのセクションを開くし、クライアントが読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。 
    
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

**IMAPISession::OpenProfileSection**メソッドは、プロファイルのセクションまたは**IProfSect**インターフェイスをサポートするオブジェクトを開きます。 プロファイルのセクションでは、情報の読み込みおよびセッション ・ プロファイル情報を書き込むのために使用されます。 
  
_UlFlags_パラメーターで MAPI_FORCE_ACCESS を指定しない限り、その個々 のサービス プロバイダーを独自でプロファイルのセクションを開くには、 **OpenProfileSection**を使用することはできません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数のクライアントが読み取り専用のアクセス許可を持つプロファイル セクションを開くことができますが、1 つのクライアントは、読み取り/書き込みアクセス許可を持つプロファイル セクションを開くことができます。 プロファイルのセクションを開くには、MAPI_MODIFY フラグを設定して**OpenProfileSection**を呼び出すことで開こうとすると、別のクライアントの場合は、MAPI_E_NO_ACCESS を返す呼び出しが失敗します。 
  
セクションが書き込み用に開いている場合、読み取り専用ファイルを開く操作が失敗します。 
  
MAPI_MODIFY フラグと、 _lpUID_パラメーターに存在しない**MAPIUID**構造体の**OpenProfileSection**を呼び出すことによって、プロファイルのセクションを作成できます。 MAPI_MODIFY を指定することを確認します。 存在しない**MAPIUID**を指すように_lpUID_を設定すると、 **OpenProfileSection**は読み取り専用の既定のアクセス モードを使用する設定は、MAPI_E_NOT_FOUND の呼び出しは失敗します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


---
title: imapisessionopenプロファイルを開く
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329408"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のプロファイルのセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>パラメーター

 _lpuid_
  
> 順番プロファイルセクションを識別する[MAPIUID](mapiuid.md)構造体へのポインター。 
    
 _lpinterface_
  
> 順番プロファイルセクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、 _lppProfSect_パラメーターによって、プロファイルセクションの標準インターフェイスである**IProfSect**へのポインターが返されます。
    
 _ulFlags_
  
> 順番プロファイルセクションへのアクセスを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DEFERRED_ERRORS 
  
> 呼び出し**** 元クライアントがプロファイルセクションを完全に利用できるようになるまで、openprofile の開始を正常に戻すことができます。 プロファイルセクションを使用できない場合は、その後の呼び出しを行うとエラーが発生する可能性があります。 
    
MAPI_FORCE_ACCESS
  
> プロバイダーに属さないプロファイルセクションへのアクセスを許可します。
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、プロファイルセクションは読み取り専用のアクセス許可で開かれ、読み取り/書き込みアクセス許可が与えられているという前提でクライアントを動作させることはできません。 
    
 _lppProfSect_
  
> 読み上げプロファイルセクションへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルセクションが正常に開かれました。
    
MAPI_E_NO_ACCESS 
  
> 発信者が十分なアクセス許可を持っていないプロファイルセクションにアクセスしようとしました。
    
MAPI_E_NOT_FOUND 
  
> [要求されたプロファイル] セクションが存在しません。
    
## <a name="remarks"></a>解説

**imapisession:: openプロファイル**のメソッドは、 **IProfSect**インターフェイスをサポートするプロファイルセクションまたはオブジェクトを開きます。 プロファイルセクションは、セッションプロファイルに関する情報の読み取りおよび書き込みに使用されます。 
  
_ulflags_パラメーター **** に MAPI_FORCE_ACCESS を指定しない限り、openprofile sections を使用して、個々のサービスプロバイダーが所有するプロファイルセクションを開くことはできません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数のクライアントが読み取り専用アクセス許可でプロファイルセクションを開くことはできますが、読み取り/書き込みアクセス許可を持つプロファイルセクションを開くことができるクライアントは1つだけです。 MAPI_MODIFY フラグセットを使用して openprofile を呼び出すことによっ**** て開こうとして、別のクライアントでプロファイルセクションが開いている場合、呼び出しは失敗し、MAPI_E_NO_ACCESS が返されます。 
  
読み取り専用の開く操作は、セクションが書き込み用に開かれている場合は失敗します。 
  
MAPI_MODIFY フラグと、 _lpuid_パラメーターに存在しない**MAPIUID**構造で**openprofile**を呼び出すことで、プロファイルセクションを作成できます。 必ず MAPI_MODIFY を指定してください。 存在しない**MAPIUID**をポイントするように_lpuid_を設定し、 **openプロファイル**が読み取り専用の既定のアクセスモードを使用するように設定されている場合、呼び出しは MAPI_E_NOT_FOUND で失敗します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


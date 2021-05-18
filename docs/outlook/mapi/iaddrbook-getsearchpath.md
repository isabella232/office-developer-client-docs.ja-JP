---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412983"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドによって開始される名前解決プロセスに含めるコンテナーのエントリ識別子の順序付きリストを返します。 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]検索パスで返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _lppSearchPath_
  
> [out]コンテナー エントリ識別子の順序付きリストへのポインター。 **GetSearchPath は** 、順序付きリストを [SRowSet 構造体に格納](srowset.md) します。 アドレス帳階層にコンテナーがない場合は **、SRowSet** 構造体で 0 が返されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検索パスが正常に取得されました。
    
## <a name="remarks"></a>注釈

クライアントとサービス プロバイダーは **GetSearchPath** メソッドを呼び出して **、ResolveName** メソッドで名前を解決するために使用される検索パスを取得します。 通常、クライアントは [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) メソッドを呼び出して **、GetSearchPath** を呼び出して取得する前に、プロファイル内にコンテナー検索パスを確立します。 ただし **、SetSearchPath の呼び出し** はオプションです。 
  
**SetSearchPath が** 呼び出されたことがない場合 **、GetSearchPath** はアドレス帳の階層テーブルを操作してパスを構築します。 **GetSearchPath** によって確立される既定の検索パスは、次の順序で次のコンテナーで構成されます。 
  
1. 読み取り/書き込みアクセス許可を持つ最初のコンテナー (通常は個人用アドレス帳 (PAB) です。
    
2. そのコンテナー [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)プロパティ **が** PR_DISPLAY_TYPEに設定されているコンテナー DT_GLOBAL。 この設定は、コンテナーが受信者を保持します。 
    
3. **PR_DISPLAY_TYPE** プロパティに DT_GLOBAL フラグが設定されているコンテナーが存在し、既定のコンテナーが読み取り/書き込みアクセス許可を持つ最初のコンテナーとは異なる場合、既定として指定されたコンテナー。 
    
**SetSearchPath が** 呼び出された場合 **、GetSearchPath** はプロファイルに格納されているアドレス帳コンテナーを使用してパスを構築します。 **GetSearchPath は** 、呼び出し元に返す前に、このパスを検証します。 
  
**SetSearchPath** の最初の呼び出しの後、GetSearchPath によって返される検索パスを変更するには **、SetSearchPath** への後続の呼び出し **を使用する必要があります**。 つまり、呼び出し元のクライアントまたはプロバイダーは、SetSearchPath の最初の呼び出し後に既定の検索パス **を受け取らないのです**。
  
## <a name="see-also"></a>関連項目



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


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
  
[IAddrBook:: ResolveName](iaddrbook-resolvename.md)メソッドによって開始された名前解決プロセスに含まれるコンテナーのエントリ id の順序付きリストを返します。 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番検索パスで返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _lppSearchPath_
  
> 読み上げコンテナーエントリ識別子の順序付きリストへのポインターへのポインター。 **GetSearchPath**は、注文されたリストを[srowset](srowset.md)構造に格納します。 アドレス帳の階層にコンテナーが存在しない場合は、 **srowset**構造体に0が返されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 検索パスが正常に取得されました。
    
## <a name="remarks"></a>注釈

クライアントおよびサービスプロバイダーは、 **GetSearchPath**メソッドを呼び出して、 **ResolveName**メソッドで名前を解決するために使用される検索パスを取得します。 通常、クライアントは[IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md)メソッドを呼び出して、プロファイルにコンテナー検索パスを設定してから、 **GetSearchPath**を呼び出して取得します。 ただし、 **SetSearchPath**の呼び出しはオプションです。 
  
**SetSearchPath**が呼び出されていない場合、 **GetSearchPath**はアドレス帳の階層テーブルを使用してパスを作成します。 **GetSearchPath**によって確立される既定の検索パスは、次の順序で構成されています。 
  
1. 読み取り/書き込みアクセス許可を持つ最初のコンテナー。通常は個人用アドレス帳 (PAB)。
    
2. **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) プロパティが DT_GLOBAL に設定されているすべてのコンテナー。 この設定は、コンテナーが受信者を保持することを示します。 
    
3. **PR_DISPLAY_TYPE**プロパティに DT_GLOBAL フラグが設定されていて、既定のコンテナーが読み取り/書き込みアクセス許可を持つ最初のコンテナーと異なる場合に、既定として指定されているコンテナー。 
    
**SetSearchPath**が呼び出されている場合、 **GetSearchPath**は、プロファイルに格納されているアドレス帳のコンテナーを使用してパスを作成します。 **GetSearchPath**は、このパスを呼び出し元に返す前に検証します。 
  
**SetSearchPath**の最初の呼び出しの後、 **SetSearchPath**の以降の呼び出しを使用して、 **GetSearchPath**によって返される検索パスを変更する必要があります。 言い換えると、呼び出し元のクライアントまたはプロバイダーは、 **SetSearchPath**の最初の呼び出しの後に既定の検索パスを受信しません。
  
## <a name="see-also"></a>関連項目



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


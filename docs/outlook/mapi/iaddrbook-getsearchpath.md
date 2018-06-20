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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c20cd7f82df2fb7f878db177fdc940022e1da351
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800382"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**適用されます**: Outlook 
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドによって開始された名前解決の処理に含まれるコンテナーのエントリ id の順序付きリストを返します。 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]検索パスで返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 関数が返す文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _lppSearchPath_
  
> [out]コンテナーのエントリ id の順序付きリストへのポインターへのポインター。 **GetSearchPath** [SRowSet](srowset.md)構造体の順序付きリストを格納します。 アドレス帳の階層内のコンテナーがない場合、 **SRowSet**構造体で 0 が返されます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 検索パスが正常に取得しました。
    
## <a name="remarks"></a>備考

クライアントとサービス ・ プロバイダーは、 **ResolveName**メソッドを使用して名前を解決するために使用される検索パスを取得する**GetSearchPath**メソッドを呼び出します。 通常、クライアントは、それを取得するために**GetSearchPath**を呼び出す前に、プロファイルにコンテナーの検索パスを確立するために[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)メソッドを呼び出します。 ただし、 **SetSearchPath**の呼び出しは、省略可能です。 
  
**SetSearchPath**が呼び出されていない場合**GetSearchPath**パスを構築を通じて、アドレス帳の階層テーブルです。 **GetSearchPath**によって設定された既定の検索パスは、次の順序で次のコンテナーで構成されます。 
  
1. 個人用アドレス帳 (PAB) では通常、読み取り/書き込みアクセス許可を持つ最初のコンテナーです。
    
2. その**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) プロパティが DT_GLOBAL に設定されているすべてのコンテナーです。 この設定は、受信者コンテナーを保持していることを示します。 
    
3. DT_GLOBAL フラグが、 **PR_DISPLAY_TYPE**プロパティと既定のコンテナーに設定されているコンテナーがない場合、既定値として指定されているコンテナーは、読み取り/書き込みアクセス許可を持つ最初のコンテナーとは異なります。 
    
**SetSearchPath**が呼び出されると、 **GetSearchPath**は、プロファイルに格納されているアドレス帳コンテナーを使用してパスを作成します。 **GetSearchPath**は、呼び出し元に返す前に、このパスを検証します。 
  
**SetSearchPath**の最初の呼び出しの後に、 **GetSearchPath**によって返される検索パスを変更するのには**SetSearchPath**以降の呼び出しを使用してください。 つまり、呼び出し元のクライアントやプロバイダーは、デフォルトの検索パスを**SetSearchPath**に最初の呼び出し後受信しません。
  
## <a name="see-also"></a>関連項目



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


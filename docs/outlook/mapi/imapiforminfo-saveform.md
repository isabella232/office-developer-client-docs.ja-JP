---
title: imapiforminfosaveform
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321715"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
構成ファイルに特定のフォームの説明を保存します。
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>パラメーター

 _szfilename_
  
> 順番フォームの説明メッセージファイルの名前を示す文字列。説明は保存されます。 このファイル名には、拡張子 fdm を付ける必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_EXTENDED_ERROR 
  
> 構成ファイルを書き込めませんでした。 エラーに関連付けられている[MAPIERROR](mapierror.md)構造体を取得するには、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。 
    
MAPI_E_NO_SUPPORT 
  
> **saveform**は、ローカルフォームコンテナーにフォームを保存するために呼び出された可能性があります。 **saveform**は、ローカルフォームコンテナーではサポートされていません。 
    
## <a name="remarks"></a>解説

クライアントアプリケーションは、指定されたファイル名を持つファイルに現在のフォームの説明を保存するために、 **imapiforminfo:: saveform**メソッドを呼び出します。 **saveform**構成ファイルを作成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

フォームを再インストールするには、フォームライブラリプロバイダーが表示するダイアログボックスでフォーム記述子メッセージのリストからフォームを選択します。 フォーム記述子メッセージに推奨される拡張子は、fdm です。
  
**saveform**が MAPI_E_EXTENDED_ERROR を返す場合は、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出し、返された**MAPIERROR**構造を調べて、エラーの原因となった条件を特定します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


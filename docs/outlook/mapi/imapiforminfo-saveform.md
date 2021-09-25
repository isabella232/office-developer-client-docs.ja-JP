---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 02bb6eb7620ee57f340217b7d9a70b63ef9878ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579885"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のフォームの説明を構成ファイルに保存します。
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>パラメーター

 _szFileName_
  
> [in]説明が保存されているフォームの説明メッセージ ファイルの名前を指定する文字列。 このファイル名には、拡張子 .fdm が必要です。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_EXTENDED_ERROR 
  
> 構成ファイルを書き込む必要があります。 エラーに関連 [付けられている MAPIERROR](mapierror.md) 構造を取得するには [、IMAPIProp::GetLastError メソッドを呼び出](imapiprop-getlasterror.md) します。 
    
MAPI_E_NO_SUPPORT 
  
> ローカル フォーム コンテナーにフォームを保存するために **SaveForm** が呼び出された可能性があります。 **SaveForm** はローカル フォーム コンテナーではサポートされていません。 
    
## <a name="remarks"></a>注釈

クライアント アプリケーションは **IMAPIFormInfo::SaveForm** メソッドを呼び出して、指定されたファイル名を持つファイルに現在のフォームの説明を保存します。 **SaveForm** は構成ファイルを作成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

フォームを再インストールするには、フォーム ライブラリ プロバイダーが表示するダイアログ ボックスのフォーム記述子メッセージの一覧からフォームを選択します。 フォーム記述子メッセージの推奨拡張機能は .fdm です。
  
**SaveForm** が MAPI_E_EXTENDED_ERROR を返す場合は [IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出し、返された **MAPIERROR** 構造体をチェックして、エラーの原因となる条件を特定します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


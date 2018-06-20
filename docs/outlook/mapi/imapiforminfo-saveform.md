---
title: IMAPIFormInfoSaveForm
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5e2d757fe329f9a57447723d72a859c7d82fc2b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800545"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**適用されます**: Outlook 
  
構成ファイル内の特定のフォームの説明を保存します。
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Parameters

 _szFileName_
  
> [in]説明が保存されているフォームの説明のメッセージ ファイルの名前を示す文字列です。 このファイル名には、.fdm 拡張機能が必要です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_EXTENDED_ERROR 
  
> 構成ファイルに書き込めませんでした。 エラーに関連付けられている[MAPIERROR](mapierror.md)構造体を取得するには、 [IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。 
    
MAPI_E_NO_SUPPORT 
  
> **SaveForm**は、ローカルのフォームのコンテナー内のフォームを保存する可能性がありますと呼ばれます。 **SaveForm**は、ローカルのフォームのコンテナーではサポートされていません。 
    
## <a name="remarks"></a>備考

クライアント アプリケーションは、指定したファイル名を持つファイルの現在のフォームの説明を保存するのには**IMAPIFormInfo::SaveForm**メソッドを呼び出します。 **SaveForm**は、構成ファイルを作成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

フォーム ライブラリ プロバイダーの表示] ダイアログ ボックスでフォーム記述子メッセージの一覧から選択してフォームを再インストールすることができます。 フォーム記述子のメッセージに推奨される拡張子は、.fdm です。
  
MAPI_E_EXTENDED_ERROR、 **SaveForm**場合、 [IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出すし、エラーが発生した状態を判断するのには返された**MAPIERROR**構造体をチェックします。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)


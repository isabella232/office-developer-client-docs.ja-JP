---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351647"
---
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームライブラリにフォームをインストールします。
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、クライアントアプリケーションが_ulflags_パラメーターに MAPI_DIALOG フラグを設定していない場合は無視されます。 _uluiparam_パラメーターは、MAPI_DIALOG も渡されない場合は NULL になります。 
    
 _ulFlags_
  
> 順番フォームのインストールを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> 進捗状況の情報を提供するダイアログボックスを表示します。詳細については、ユーザーに確認します。 このフラグが設定されていない場合は、ダイアログボックスは表示されません。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> このフォームによって処理されるメッセージクラスを処理する別のフォームが既に存在する場合は、既存のフォームをこのフォームに置き換えます。 MAPI_DIALOG フラグも指定されている場合、このフラグは無視されます。 
    
 _szcfgpathname_
  
> 順番フォームの構成ファイルへのパス。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_EXTENDED_ERROR 
  
> 実装エラーが発生しました。 エラーに関連付けられている[MAPIERROR](mapierror.md)構造体を取得するには、 [imapiformcontainer:: GetLastError](imapiformcontainer-getlasterror.md)メソッドを呼び出します。 
    
MAPI_E_USER_CANCEL 
  
> ユーザーがフォームのインストールをキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="notes-to-implementers"></a>実装に関するメモ

フォームライブラリプロバイダーは、次のいずれかの状況が発生した場合に、 **MAPIERROR**構造に記入し、MAPI_E_EXTENDED_ERROR を返す必要があります。 
  
- 構成ファイルが見つかりません。
    
- 構成ファイルは読み取ることができません。
    
- 構成ファイルが無効です。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

クライアントアプリケーションは、 **imapiformcontainer:: installform**メソッドを呼び出して、特定のフォームコンテナーにフォームをインストールします。 _szcfgpathname_パラメーターには、フォーム構成ファイル (つまり、フォームとその実装を記述する拡張子が付いたファイル) のパスを含める必要があります。 _ulflags_パラメーターのフラグには、次のものを指定します。 
  
- MAPI_DIALOG フラグが設定されている場合は、ユーザーインターフェイスが表示され、フォームをインストールしているユーザーがインストールの詳細を指定できます。
    
- MAPIFORM_INSTALL_OVERWRITEONCONFLICT フラグが設定されている場合、同じメッセージクラスの以前のフォームは、インストールされているフォームに置き換えられます。 それ以外の場合は、フォームのインストールは現在のフォームの説明に結合されます (存在する場合)。
    
- MAPI_DIALOG が設定されている場合、MAPIFORM_INSTALL_OVERWRITEONCONFLICT は無視されます。
    
- フラグセットに MAPIFORM_INSTALL_OVERWRITEONCONFLICT がない場合は、マージが行われることを意味します。 現在フォームの説明に表示されていない、cfg ファイルの新しいプラットフォームがインストールされ、その他の変更は行われません。
    
- MAPI_UNICODE フラグが設定されている場合、フォーム構成ファイルのパスは UNICODE 文字列になります。 
    
クライアントは[imapiformcontainer:: GetLastError](imapiformcontainer-getlasterror.md)を呼び出し**** て MAPI_E_EXTENDED_ERROR を返す必要があり、返された[MAPIERROR](mapierror.md)構造を調べて、エラーが発生した条件を特定する必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FormContainerDlg  <br/> |CFormContainerDlg:: oninstallform  <br/> |mfcmapi は、 **imapiformcontainer:: installform**メソッドを使用してフォームコンテナーにフォームをインストールします。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)


---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f8f5db6ebb264788de6a9c8a570056c3d8ace8e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621004"
---
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム ライブラリにフォームをインストールします。
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは、クライアント アプリケーションが _ulFlags_ パラメーターに MAPI_DIALOGフラグを設定しない限り無視されます。 _ulUIParam_ パラメーターは、パラメーターも渡MAPI_DIALOG NULL を指定できます。 
    
 _ulFlags_
  
> [in]フォームのインストールを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_DIALOG 
  
> ダイアログ ボックスを表示して、進行状況情報を提供するか、ユーザーに詳細を求めるプロンプトを表示します。 このフラグが設定されていない場合、ダイアログ ボックスは表示されません。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> このフォームで処理されるメッセージ クラスを処理する別のフォームが既に存在する場合は、既存のフォームをこのフォームに置き換える必要があります。 このフラグは、MAPI_DIALOGが存在する場合は無視されます。 
    
 _szCfgPathName_
  
> [in]フォームの構成ファイルへのパス。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_EXTENDED_ERROR 
  
> 実装エラーが発生しました。 エラーに関連 [付けられている MAPIERROR](mapierror.md) 構造を取得するには [、IMAPIFormContainer::GetLastError メソッドを呼び出](imapiformcontainer-getlasterror.md) します。 
    
MAPI_E_USER_CANCEL 
  
> ユーザーは、通常、ダイアログ ボックスの [キャンセル] ボタンをクリックして、フォームのインストールをキャンセルしました。 
    
## <a name="notes-to-implementers"></a>実装に関するメモ

フォーム ライブラリ プロバイダーは **、MAPIERROR** 構造を入力し、次MAPI_E_EXTENDED_ERROR条件が発生した場合は、このプロパティを返す必要があります。 
  
- 構成ファイルが見つかりません。
    
- 構成ファイルは読み取り可能ではありません。
    
- 構成ファイルが無効です。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

クライアント アプリケーションは **IMAPIFormContainer::InstallForm** メソッドを呼び出して、フォームを特定のフォーム コンテナーにインストールします。 _szCfgPathName_ パラメーターには、フォーム構成ファイルのパス (つまり、フォームとその実装を記述する .cfg 拡張子を持つファイル) が含まれている必要があります。 _ulFlags パラメーターのフラグ_ は、次の値を指定します。 
  
- [MAPI_DIALOG] フラグが設定されている場合は、ユーザー インターフェイスが表示され、フォームをインストールするユーザーがインストールの詳細を指定できます。
    
- このフラグMAPIFORM_INSTALL_OVERWRITEONCONFLICT設定すると、同じメッセージ クラスの前のフォームがインストールされているフォームに置き換えられる。 それ以外の場合、フォームのインストールは、現在のフォームの説明 (存在する場合) と結合されます。
    
- このMAPI_DIALOG設定されている場合、MAPIFORM_INSTALL_OVERWRITEONCONFLICTは無視されます。
    
- フラグ セットにMAPIFORM_INSTALL_OVERWRITEONCONFLICTがない場合は、マージが行われます。 フォームの説明に現在存在しない .cfg ファイル内の新しいプラットフォームはインストールされ、その他の変更は行われません。
    
- このフラグMAPI_UNICODE設定すると、フォーム構成ファイルのパスは Unicode 文字列になります。 
    
InstallForm が MAPI_E_EXTENDED_ERROR を返す場合、クライアントは[IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md)を呼び出す必要があります。エラーが発生した条件を判断するには、返された[MAPIERROR](mapierror.md)構造を確認する必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI は **IMAPIFormContainer::InstallForm** メソッドを使用してフォーム コンテナーにフォームをインストールします。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)


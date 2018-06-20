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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d329d3a14b6026d0bd62df9feba6ccff251e4151
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800524"
---
# <a name="imapiformcontainerinstallform"></a>IMAPIFormContainer::InstallForm

  
  
**適用されます**: Outlook 
  
フォーム ライブラリにフォームをインストールします。
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。 _UlUIParam_パラメーターは、クライアント アプリケーションは、 _ulFlags_パラメーターで MAPI_DIALOG フラグを設定しない限り、無視されます。 MAPI_DIALOG が渡されてもいない場合は、 _ulUIParam_パラメーターを NULL にできます。 
    
 _ulFlags_
  
> [in]フォームのインストールを制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DIALOG 
  
> 進行状況情報を提供したり、詳細情報をユーザーに確認するダイアログ ボックスが表示されます。 このフラグが設定されていない場合、ダイアログ ボックスは表示されません。
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
MAPIFORM_INSTALL_OVERWRITEONCONFLICT 
  
> 別のフォームによって、メッセージ クラスは、このフォームで処理するハンドルが既に存在する場合は、既存のフォームをこれと置き換えます。 MAPI_DIALOG フラグが存在しても場合、このフラグは無視されます。 
    
 _szCfgPathName_
  
> [in]フォームの構成ファイルへのパス。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_EXTENDED_ERROR 
  
> 実装エラーが発生しました。 エラーに関連付けられている[MAPIERROR](mapierror.md)構造体を取得するには、 [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md)メソッドを呼び出します。 
    
MAPI_E_USER_CANCEL 
  
> ユーザー] ダイアログ ボックスで [**キャンセル**] ボタンをクリックすると、通常、フォームのインストールをキャンセルしました。 
    
## <a name="notes-to-implementers"></a>実装者へのメモ

フォーム ライブラリのプロバイダーは、 **MAPIERROR**構造体を入力し、次の条件のいずれかが発生した場合は、MAPI_E_EXTENDED_ERROR を返す必要があります。 
  
- 構成ファイルが見つかりません。
    
- 構成ファイルを読み取ることができません。
    
- 構成ファイルが有効ではありません。
    
## <a name="notes-to-callers"></a>呼び出し側への注意

クライアント アプリケーションは、フォームをフォームの特定のコンテナーにインストールするのには**IMAPIFormContainer::InstallForm**メソッドを呼び出します。 _SzCfgPathName_パラメーターには、フォーム構成ファイル (つまり、フォームとその実装を記述する .cfg ファイルの拡張子を持つファイルの場合) のパスが含まれている必要があります。 _UlFlags_パラメーター内のフラグは、以下のいずれかを指定します。 
  
- MAPI_DIALOG フラグが設定されている場合は、ユーザー インターフェイスが表示されます、インストールの詳細を指定するフォームをインストールしているユーザーを有効にします。
    
- MAPIFORM_INSTALL_OVERWRITEONCONFLICT フラグが設定されている場合は、同じメッセージ クラスのすべての前のフォームがインストールされているフォームに置き換えられます。 それ以外の場合、フォームのインストールは、存在する場合、現在のフォームの説明に統合されます。
    
- MAPI_DIALOG が設定されている場合は、MAPIFORM_INSTALL_OVERWRITEONCONFLICT は無視されます。
    
- MAPIFORM_INSTALL_OVERWRITEONCONFLICT のフラグでない場合は、差し込み印刷が行われることを意味を設定します。 .Cfg ファイルの現在のフォームの説明ではない新しいプラットフォームをインストールして、その他の変更は行われません。
    
- フォーム構成ファイルのパスは、MAPI_UNICODE フラグが設定されている場合は、Unicode 文字列になります。 
    
**InstallForm**は、MAPI_E_EXTENDED_ERROR を返し、エラーが発生した状態を判断するのには返された[MAPIERROR](mapierror.md)構造体をチェックする必要がある場合、クライアントは[IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md)を呼び出す必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnInstallForm  <br/> |MFCMAPI では、 **IMAPIFormContainer::InstallForm**メソッドを使用して、フォームのコンテナー内のフォームをインストールします。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)


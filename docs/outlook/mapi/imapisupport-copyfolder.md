---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0b079b311a68459a43b0a7659ddfbe94d96d7f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800721"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**適用対象**: Outlook 
  
現在の親フォルダーから別の親フォルダーにフォルダーを移動またはコピーします。
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpSrcInterface_
  
> [in]コピーまたは移動するフォルダーの親フォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpSrcFolder_
  
> [in]コピーまたは移動するフォルダーの親フォルダーへのポインター。 
    
 _cbEntryID_
  
> [in]_LpEntryID_で指定されたエントリの識別子のバイト数です。
    
 _lpEntryID_
  
> [in]コピーまたは移動するフォルダーのエントリの識別子へのポインター。 
    
 _lpInterface_
  
> [in]予約されています。NULL である必要があります。
    
 _lpDestFolder_
  
> [in]コピーまたは移動するフォルダーを受信するフォルダーへのポインター。
    
 _lpszNewFolderName_
  
> [in]コピーまたは移動したフォルダーの名前へのポインターそれ以外の場合、NULL、コピーまたは移動したフォルダーがソース フォルダー ( _lpEntryID_で指定されたフォルダー) と同じ名前を持つ必要があることを示します。
    
 _ulUIParam_
  
> [in]進行状況インジケーターのダイアログ ボックスのウィンドウと関連するウィンドウのハンドルです。 _UlFlags_パラメーターに FOLDER_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。 _LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。 _UlFlags_に FOLDER_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。
    
 _ulFlags_
  
> [in]コピーまたは移動操作を実現する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
COPY_SUBFOLDERS 
  
> すべてのフォルダーのサブフォルダーは、コピーまたは移動する必要があります。 コピー操作のために COPY_SUBFOLDERS が設定されていない場合は、 _lpEntryID_によって識別されたフォルダーのみがコピーされます。 移動操作で、COPY_SUBFOLDERS の動作は既定のフラグが設定されているかどうかに関係なくです。 
    
FOLDER_DIALOG 
  
> 進行状況インジケーターの表示を要求します。
    
FOLDER_MOVE 
  
> フォルダーの移動の代わりにコピーします。 FOLDER_MOVE が設定されていない場合、フォルダーをコピーします。
    
MAPI_UNICODE 
  
> フォルダーの名前は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のフォルダーの名前です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フォルダーは正常にコピーまたは移動されています。
    
MAPI_E_COLLISION 
  
> 移動またはコピーされているフォルダーの名前は、コピー先のフォルダーのサブフォルダーの名前と同じです。 メッセージ ストア プロバイダーは、フォルダー名が一意である必要があります。 完了せず、操作を停止します。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しが成功したが、すべてのエントリが正常にコピーされました。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::CopyFolder**メソッドを実装します。 メッセージ ストア プロバイダーは、コピーまたは別の 1 つの親フォルダーから 1 つのフォルダーを移動する[IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)の実装では、 **IMAPISupport::CopyFolder**を呼び出すことができます。 
  
 **IMAPISupport::CopyFolder**は、コピー先のフォルダーのサブフォルダーとしてコピーまたは移動したフォルダーを追加します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **IMAPISupport::CopyFolder**は、名前を変更してフォルダーと、コピーまたは移動の影響を受けるフォルダーのサブフォルダーの移動を同時に使用できます。 コピーまたは移動、コピーまたは移動したフォルダーにネストされたすべてのサブフォルダー、 _ulFlags_で COPY_SUBFOLDERS フラグを渡します。 
  
次に、次の条件の値を返すことを期待される結果します。
  
|**条件**|**戻り値**|
|:-----|:-----|
|**CopyFolder**は正常にコピーまたは適用可能な場合、フォルダーとそのすべてのサブフォルダーを移動します。  <br/> |S_OK  <br/> |
|**CopyFolder**は、正常にコピーまたはすべてのフォルダーを移動できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder**は完了できませんでした。  <br/> |エラー値  <br/> |
   
**CopyFolder**では、エラー値が返された場合は、作業が実行されなかったことを想定しては続行できません。 1 つまたは複数のフォルダーでしたコピーされたり、 **CopyFolder**にエラーが発生した前に移動します。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)


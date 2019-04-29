---
title: imapisupportcopyfolder
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420886"
---
# <a name="imapisupportcopyfolder"></a>IMAPISupport::CopyFolder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーを現在の親フォルダーから別の親フォルダーにコピーまたは移動します。
  
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

 _lpsrcinterface_
  
> 順番コピーまたは移動するフォルダーの親フォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpsrcfolder_
  
> 順番コピーまたは移動するフォルダーの親フォルダーへのポインター。 
    
 _cbEntryID_
  
> 順番エントリ識別子のバイト数が_lな tryid_で示されます。
    
 _lて tryid_
  
> 順番コピーまたは移動するフォルダーのエントリ識別子へのポインター。 
    
 _lpinterface_
  
> 順番予約語NULL である必要があります。
    
 _lpdestfolder_
  
> 順番コピーまたは移動するフォルダーを受け取るフォルダーへのポインター。
    
 _lpsznewfoldername_
  
> 順番コピーまたは移動したフォルダーの名前へのポインター。それ以外の場合は、コピーまたは移動されたフォルダーの名前がソースフォルダーと同じであることを示します ( _lな tryid_で示されるフォルダー)。
    
 _uluiparam_
  
> 順番[進行状況インジケーター] ダイアログボックスと関連するウィンドウのウィンドウのハンドル。 _uluiparam_パラメーターは、 _ulflags_パラメーターで FOLDER_DIALOG フラグが設定されていない場合は無視されます。 
    
 _lpprogress_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター。 _lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 FOLDER_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。
    
 _ulFlags_
  
> 順番コピー操作または移動操作の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
COPY_SUBFOLDERS 
  
> すべてのフォルダーのサブフォルダーをコピーまたは移動する必要があります。 コピー操作で COPY_SUBFOLDERS が設定されていない場合は、 _l tryid_で識別されるフォルダーのみがコピーされます。 移動操作では、フラグが設定されているかどうかに関係なく、COPY_SUBFOLDERS の動作が既定値になります。 
    
FOLDER_DIALOG 
  
> 進行状況インジケーターの表示を要求します。
    
FOLDER_MOVE 
  
> フォルダーはコピーではなく移動する必要があります。 FOLDER_MOVE が設定されていない場合は、フォルダーがコピーされます。
    
MAPI_UNICODE 
  
> フォルダーの名前は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、フォルダーの名前は ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォルダーが正常にコピーまたは移動されました。
    
MAPI_E_COLLISION 
  
> 移動またはコピーするフォルダーの名前が、移動先フォルダーのサブフォルダーの名前と同じです。 メッセージストアプロバイダーでは、フォルダー名が一意である必要があります。 操作は完了せずに停止します。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのエントリが正常にコピーされませんでした。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>注釈

**imapisupport:: copyfolder**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。 メッセージストアプロバイダーは、 [imapisupport:](imapifolder-copyfolder.md) : copyfolder の実装で**imapisupport:: copyfolder**を呼び出して、1つの親フォルダーから別のフォルダーに1つのフォルダーをコピーまたは移動することができます。 
  
 **imapisupport:: copyfolder**移動先フォルダーのサブフォルダーとして、コピーまたは移動したフォルダーを追加します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **imapisupport:: copyfolder**を使用すると、フォルダーの名前変更と移動、および影響を受けたフォルダーのサブフォルダーのコピーまたは移動を同時に行うことができます。 コピーまたは移動したフォルダーでネストされているすべてのサブフォルダーをコピーまたは移動するには、COPY_SUBFOLDERS フラグを_ulflags_に渡します。 
  
次の条件下では、次の戻り値が予想されます。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**** 必要に応じて、フォルダーとそのすべてのサブフォルダーがコピーまたは移動されました。  <br/> |S_OK  <br/> |
|**copyfolder**は、すべてのフォルダーを正常にコピーまたは移動できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**copyfolder**を完了できませんでした。  <br/> |任意のエラー値  <br/> |
   
**copyfolder**がエラー値を返した場合は、処理が行われていないという前提で続行しないでください。 **copyfolder**でエラーが発生する前に、1つ以上のフォルダーがコピーまたは移動された可能性があります。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)


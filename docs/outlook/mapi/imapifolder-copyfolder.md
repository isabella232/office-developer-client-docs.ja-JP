---
title: imapifoldercopyfolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280179"
---
# <a name="imapifoldercopyfolder"></a>IMAPIFolder::CopyFolder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サブフォルダーをコピーまたは移動します。
  
```cpp
HRESULT CopyFolder(
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

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番コピーまたは移動するサブフォルダーのエントリ識別子へのポインター。
    
 _lpinterface_
  
> 順番_lpdestfolder_パラメーターが指すフォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、サービスプロバイダーは標準のフォルダーインターフェイス、 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)を返します。 _lpinterface_の有効な値は、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、および IID_IMAPIFolder です。 
    
 _lpdestfolder_
  
> 順番コピーまたは移動したサブフォルダーを受け取るための、開いているフォルダーへのポインター。
    
 _lpsznewfoldername_
  
> 順番コピーまたは移動先のフォルダーの名前へのポインター。 _lpsznewfoldername_が NULL に設定されている場合、source サブフォルダーの名前が宛先フォルダーの名前として使用されます。 
    
 _uluiparam_
  
> 順番進行状況インジケーターの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、 _ulflags_パラメーターの FOLDER_DIALOG フラグが設定されていない場合は無視されます。 
    
 _lpprogress_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター。 _lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 FOLDER_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。
    
 _ulFlags_
  
> 順番コピー操作または移動操作を制御するフラグのビットマスク。 次のフラグを設定できます。
    
COPY_SUBFOLDERS 
  
> コピーするサブフォルダー内のすべてのサブフォルダーもコピーする必要があります。 コピー操作で COPY_SUBFOLDERS が設定されていない場合は、 _l tryid_で識別されるサブフォルダーのみがコピーされます。 移動操作では、フラグが設定されているかどうかに関係なく、COPY_SUBFOLDERS の動作が既定値になります。 
    
FOLDER_DIALOG 
  
> 進行状況インジケーターの表示を要求します。
    
FOLDER_MOVE 
  
> サブフォルダーはコピーではなく移動されます。 FOLDER_MOVE が設定されていない場合は、サブフォルダーがコピーされます。
    
MAPI_DECLINE_OK 
  
> サポートオブジェクトの imapisupport を呼び出して**copyfolder**を実装する場合に、メッセージストアプロバイダーに通知します[。:D ocopyto](imapisupport-docopyto.md)または[imapisupport::D ocopyprops](imapisupport-docopyprops.md)メソッド、 **copyfolder**はすぐに MAPI_E_ を返す必要があります。DECLINE_COPY。 
    
MAPI_UNICODE 
  
> 宛先フォルダーの名前は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、フォルダー名は ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定したフォルダーが正常にコピーまたは移動されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されており、メッセージストアプロバイダーが unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、メッセージストアプロバイダーが unicode のみをサポートしています。
    
MAPI_E_COLLISION 
  
> 移動またはコピーするフォルダーの名前が、移動先フォルダーのサブフォルダーの名前と同じです。 メッセージストアプロバイダーには、一意のフォルダー名が必要です。
    
MAPI_E_DECLINE_COPY 
  
> プロバイダーは、サポートオブジェクトのメソッドを呼び出すことによってこのメソッドを実装し、発信者が MAPI_DECLINE_OK フラグを渡しています。
    
MAPI_E_FOLDER_CYCLE 
  
> ソースフォルダーが直接または間接的に、宛先フォルダーを含んでいる。 この条件が検出される前に、重要な作業が実行されている可能性があるため、ソースフォルダーと宛先フォルダーの一部が変更されている可能性があります。 
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのエントリが正常にコピーされませんでした。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**imapifolder:: copyfolder**メソッドは、ある場所から別の場所にサブフォルダーをコピーまたは移動します。 コピーまたは移動しているサブフォルダーは、サブフォルダーとして、宛先フォルダーに追加されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

コピー操作または移動操作で、COPY_SUBFOLDERS フラグを設定することによって複数のフォルダーが含まれている場合は、その操作を各フォルダーで可能な限り完全に実行します。 移動またはコピーするフォルダーの1つが存在しない場合や、別の場所に移動またはコピーされている場合があります。 メモリが不足している、ディスクの空き領域が不足している、メッセージストアが破損しているなど、操作を途中で停止しないようにしてください。
  
コピーしたメッセージのすべてのメッセージエントリ識別子を保持するようにしてください。 また、エントリ識別子を保持する必要はありませんが、これは必須ではありません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

これらの戻り値は、次の条件に当てはまることが予想されます。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**copyfolder**は、メッセージとサブフォルダーごとに正常にコピーまたは移動されました。  <br/> |S_OK  <br/> |
|**copyfolder**は、すべてのメッセージとサブフォルダを正常にコピーまたは移動できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND  <br/> |
|**copyfolder**を完了できませんでした。  <br/> |MAPI_E_NOT_FOUND を除くすべてのエラー値  <br/> |
   
**copyfolder**を完了できない場合でも、作業が行われていないとは限りません。 エラーが発生する前に、 **copyfolder**が1つ以上のメッセージとサブフォルダーをコピーまたは移動できた可能性があります。 
  
存在しないフォルダーのエントリ識別子が_lMAPI_W_PARTIAL_COMPLETION tryid_で渡された場合、 **copyfolder**は、メッセージストアの実装に応じて、または MAPI_E_NOT_FOUND を返します。 
  
メッセージストアプロバイダーによっては、元のメッセージのエントリ識別子がコピーされたメッセージに保持されている場合があります。 可能な限り、エントリ識別子は保持する必要がありますが、必須ではありません。 通常は、次のシナリオに依存します。
  
- 2つの異なる種類のメッセージストア間でフォルダーを移動する場合、エントリ識別子の変更は保証されます。
    
- 同じ種類の2つのメッセージストア間でフォルダーを移動する場合、エントリ識別子はほぼ常に変更されます。
    
- フォルダーを同じメッセージストア内の別の場所に移動すると、メッセージストアプロバイダーによっては、エントリ識別子が変更されない場合があります。
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg  <br/> |CMsgStoreDlg:: OnPasteFolder  <br/> |mfcmapi は、 **imapifolder:: copyfolder**メソッドを使用して、フォルダーをある場所から別の場所にコピーします。 mfcmapi はコピー操作中にソースフォルダーを記憶し、貼り付け操作中にコピーを実際に実行します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)


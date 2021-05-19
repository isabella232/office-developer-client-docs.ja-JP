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
  
現在の親フォルダーから別の親フォルダーにフォルダーをコピーまたは移動します。
  
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
  
> [in]コピーまたは移動するフォルダーの親フォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。
    
 _lpSrcFolder_
  
> [in]コピーまたは移動するフォルダーの親フォルダーへのポインター。 
    
 _cbEntryID_
  
> [in]  _lpEntryID_ が指すエントリ識別子のバイト 数です。
    
 _lpEntryID_
  
> [in]コピーまたは移動するフォルダーのエントリ識別子へのポインター。 
    
 _lpInterface_
  
> [in]予約済み。NULL である必要があります。
    
 _lpDestFolder_
  
> [in]コピーまたは移動するフォルダーを受信するフォルダーへのポインター。
    
 _lpszNewFolderName_
  
> [in]コピーまたは移動されたフォルダーの名前へのポインター。それ以外の場合は、コピーまたは移動されたフォルダーがソース フォルダー  _(lpEntryID_ によって指されるフォルダー) と同じ名前を持つ必要があります。
    
 _ulUIParam_
  
> [in]進行状況インジケーター ダイアログ ボックスと関連するウィンドウのウィンドウのハンドル。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター FOLDER_DIALOGフラグが設定されていない限り、無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。 _lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 _lpProgress パラメーター_ は _、ulFlags_ で FOLDER_DIALOGフラグが設定されていない限り無視されます。
    
 _ulFlags_
  
> [in]コピーまたは移動操作の実行方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
COPY_SUBFOLDERS 
  
> フォルダーのすべてのサブフォルダーをコピーまたは移動する必要があります。 コピー COPY_SUBFOLDERS設定されていない場合は  _、lpEntryID_ で識別されるフォルダーだけがコピーされます。 移動操作では、フラグCOPY_SUBFOLDERSに関係なく、既定の動作になります。 
    
FOLDER_DIALOG 
  
> 進行状況インジケーターの表示を要求します。
    
FOLDER_MOVE 
  
> フォルダーはコピーの代わりに移動する必要があります。 このFOLDER_MOVE設定されていない場合は、フォルダーがコピーされます。
    
MAPI_UNICODE 
  
> フォルダーの名前は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、フォルダーの名前は ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォルダーが正常にコピーまたは移動されました。
    
MAPI_E_COLLISION 
  
> 移動またはコピーされるフォルダーの名前は、移動先フォルダー内のサブフォルダーの名前と同じです。 メッセージ ストア プロバイダーでは、フォルダー名が一意である必要があります。 操作は完了せずに停止します。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのエントリが正常にコピーされたという訳ではありません。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPISupport::CopyFolder** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 メッセージ ストア プロバイダーは [、IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)の実装で **IMAPISupport::CopyFolder** を呼び出して、1 つのフォルダーを 1 つの親フォルダーから別の親フォルダーにコピーまたは移動できます。 
  
 **IMAPISupport::CopyFolder は** 、コピーまたは移動されたフォルダーを移動先フォルダーのサブフォルダーとして追加します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **IMAPISupport::CopyFolder** を使用すると、フォルダーの名前の変更と移動、および影響を受けるフォルダーのサブフォルダーのコピーまたは移動を同時に実行できます。 コピーまたは移動したフォルダーに入れ子になったすべてのサブフォルダーをコピーまたは移動するには  _、ulFlags_ の COPY_SUBFOLDERS フラグを渡します。 
  
次の条件の下で、次の戻り値を期待します。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**CopyFolder は** 、該当する場合は、フォルダーとそのすべてのサブフォルダーを正常にコピーまたは移動しました。  <br/> |S_OK  <br/> |
|**CopyFolder** は、すべてのフォルダーを正常にコピーまたは移動できなかった。  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**CopyFolder** を完了できません。  <br/> |エラー値  <br/> |
   
**CopyFolder がエラー** 値を返す場合は、作業が完了していないという前提で続行しません。 **CopyFolder** でエラーが発生する前に、1 つ以上のフォルダーがコピーまたは移動されている可能性があります。 
  
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)


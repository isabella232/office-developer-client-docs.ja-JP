---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d6f5a0bd5da851c5107b8d3d40d683a7e3c1b26b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586012"
---
# <a name="hropenabentrywithprovideruidsupport"></a>HrOpenABEntryWithProviderUIDSupport

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**HrOpenABEntryWithProviderUIDSupport**関数は、セッションとアドレス帳を使用する代わりに特定のサポート オブジェクトを使用してエントリを開きますが、 [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)関数と同じ機能を実行します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>パラメーター

 _pEmsabpUID_
  
> [in]エントリ id の詳細を表示するのにはこの関数を使用する必要があります Exchange のアドレス帳プロバイダーを識別する_emsabpUID_のパラメーターへのポインター。 受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子ではない場合は、このパラメーターは無視され、 [IAddrBook::Details](iaddrbook-details.md)関数の呼び出しの動作とまったく同じです。 このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数はまた[IAddrBook::Details](iaddrbook-details.md)と同様に機能します。
    
 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。
    
 _lpInterface_
  
> [in][Open] エントリにアクセスするために使用するインターフェイスのインターフェイス id (IID) へのポインター。 NULL を渡すことは、標準的なオブジェクトのインターフェイスを返します。 メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。 配布リストには、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)とは、コンテナーの[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。 呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。 
    
 _ulFlags_
  
> [in]_LpszButtonText_パラメーターのテキストの種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。 
    
AB_TELL_DETAILS_CHANGE
  
> 詳細は TRUE を返す場合は、アドレスに変更を加えた実際にことを示します。それ以外の場合、詳細は、FALSE を返します。
    
DIALOG_MODAL
  
> 共通のアドレス] ダイアログ ボックスのモーダル バージョンが表示されます。 このフラグは、DIALOG_SDI と相互に排他的です。
    
DIALOG_SDI
  
> モードレスのバージョンの共通のアドレス] ダイアログ ボックスが表示されます。 このフラグは、DIALOG_MODAL と相互に排他的です。
    
MAPI_UNICODE
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _lpulObjType_
  
> [out]開かれているエントリの種類へのポインター。
    
 _lppUnk_
  
> [out]開かれているエントリのポインターへのポインター。
    


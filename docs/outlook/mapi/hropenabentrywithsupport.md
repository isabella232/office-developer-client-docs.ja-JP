---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2ae4586d08eb83ebe50e1cbc2661b049b28c6cc7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576157"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この関数は使用しません。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>パラメーター

 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。 
    
 _lpEntryID_
  
> [in]開くアドレス帳エントリを表すエントリ識別子へのポインター。
    
 _lpInterface_
  
>  [in]開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。 NULL を渡す場合は、オブジェクトの標準インターフェイスを返します。 メッセージング ユーザーの場合、標準インターフェイスは [IMailUser : IMAPIProp です](imailuserimapiprop.md)。 配布リストの場合 [、IDistList : IMAPIContainer](idistlistimapicontainer.md)であり、コンテナーの場合は [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。 呼び出し元は  _、lpInterface を_ 適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。 
    
 _ulFlags_
  
> [in]  _lpszButtonText_ パラメーターのテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
AB_TELL_DETAILS_CHANGE
  
> アドレスに実際に変更が加えた場合、Details は TRUE を返します。それ以外の場合、Details は FALSE を返します。
    
DIALOG_MODAL
  
> [共通アドレス] ダイアログ ボックスのモーダル バージョンを表示します。 このフラグは、このフラグと相互にDIALOG_SDI。
    
DIALOG_SDI
  
> [共通アドレス] ダイアログ ボックスのモードレス バージョンを表示します。 このフラグは、他のフラグと相互DIALOG_MODAL。
    
MAPI_UNICODE
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _lpulObjType_
  
> [out]開いたエントリの種類へのポインター。
    
 _lppUnk_
  
> [out]開いたエントリのポインターへのポインター。
    


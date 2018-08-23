---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 262b1aa2cd4a785b612ac0917b4b24358742ea6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800329"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**適用対象**: Outlook 
  
この関数を使用することはしません。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。
    
 _lpInterface_
  
>  [in][Open] エントリにアクセスするために使用するインターフェイスのインターフェイス id (IID) へのポインター。 NULL を渡すことは、標準的なオブジェクトのインターフェイスを返します。 メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。 配布リスト、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)では、コンテナー、および[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。 呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。 
    
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
    


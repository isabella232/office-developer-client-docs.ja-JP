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
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347762"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この関数は使用しないでください。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |abhelp .h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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

 _lpsup_
  
> 
    
 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。 
    
 _lて tryid_
  
> 順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。
    
 _lpinterface_
  
>  順番開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、オブジェクトの標準インターフェイスが返されます。 メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。 配布リストの場合、 [idistlist: IMAPIContainer](idistlistimapicontainer.md)、およびコンテナーの場合は、 [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)になります。 呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。 
    
 _ulFlags_
  
> 順番_lpszbuttontext_パラメーターのテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
AB_TELL_DETAILS_CHANGE
  
> 住所に変更が実際に加えられた場合に、詳細が TRUE を返すことを示します。それ以外の場合、詳細は FALSE を返します。
    
DIALOG_MODAL
  
> [共通アドレス] ダイアログボックスのモーダルバージョンが表示されます。 このフラグは、DIALOG_SDI とは相互に排他的です。
    
DIALOG_SDI
  
> [共通アドレス] ダイアログボックスのモードレスバージョンが表示されます。 このフラグは、DIALOG_MODAL とは相互に排他的です。
    
MAPI_UNICODE
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _lpulobjtype_
  
> 読み上げ開かれた項目の種類へのポインター。
    
 _lppunk_
  
> 読み上げ開かれたエントリのポインターへのポインター。
    


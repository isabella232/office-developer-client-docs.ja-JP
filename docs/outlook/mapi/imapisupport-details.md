---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d641412a631b60c8f113555b20268cdefb94f2d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630671"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のアドレス帳エントリに関する詳細を表示するダイアログ ボックスを表示します。
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulUIParam_
  
> [out]返されるダイアログ ボックスの親ウィンドウへのハンドルへのポインター。
    
 _lpfnDismiss_
  
> [in] [DISMISSMODELESS](dismissmodeless.md) プロトタイプまたは NULL に基づく関数へのポインター。 このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。 MAPI は、ユーザーがモードレス アドレス ダイアログ ボックスを閉じ **、IMAPISupport::D** ダイアログ ボックスがアクティブでなくなったことを示すクライアントに通知するときに **、DISMISSMODELESS** 関数を呼び出します。 
    
 _lpvDismissContext_
  
> [in]_lpfnDismiss_ パラメーターが指す **DISMISSMODELESS** 関数に渡すコンテキスト情報へのポインター。 このパラメーターは  _、ulFlags_ パラメーターに DIALOG_SDIフラグを含めて、ダイアログ ボックスのモードレス バージョンにのみ適用されます。 
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]詳細が表示されるエントリ識別子へのポインター。
    
 _lpfButtonCallback_
  
> [in] [LPFNBUTTON 関数プロトタイプに基づく関数への](lpfnbutton.md) ポインター。 **LPFNBUTTON 関数は**、詳細ダイアログ ボックスにボタンを追加します。 
    
 _lpvButtonContext_
  
> [in]  _lpfButtonCallback_ パラメーターで指定された関数のパラメーターとして使用されるデータへのポインター。 
    
 _lpszButtonText_
  
> [in]そのボタンが拡張可能な場合、追加されたボタンに適用されるテキストを含む文字列へのポインター。 _拡張可能なボタンが必要ない場合、lpszButtonText_ パラメーターは NULL である必要があります。 
    
 _ulFlags_
  
> [in]  _lpszButtonText_ パラメーターのテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
DIALOG_MODAL
  
> [共通アドレス] ダイアログ ボックスのモーダル バージョンを表示します。 このフラグは、このフラグと相互にDIALOG_SDI。
    
DIALOG_SDI
  
>  [共通アドレス] ダイアログ ボックスのモードレス バージョンを表示します。 このフラグは、他のフラグと相互DIALOG_MODAL。 
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アドレス帳エントリの詳細ダイアログ ボックスが正常に表示されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::D etails** メソッドは、アドレス帳プロバイダーのサポート オブジェクトに実装されます。 アドレス帳プロバイダーは、詳細を **呼** び出して、アドレス帳内の特定のエントリの詳細を示すダイアログ ボックスを表示します。 _lpfButtonCallback_ パラメーター _、lpvButtonContext_ パラメーター、_および lpszButtonText_ パラメーターを使用して、ダイアログ ボックスにクライアント定義ボタンを追加できます。 ボタンをクリックすると、MAPI は  _lpfButtonCallback_ が指すコールバック関数を呼び出し、ボタンのエントリ識別子と  _lpvButtonContext_ のデータの両方を渡します。 拡張可能なボタンが必要ない場合  _、lpszButtonText_ は NULL である必要があります。 
  
## <a name="see-also"></a>関連項目



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


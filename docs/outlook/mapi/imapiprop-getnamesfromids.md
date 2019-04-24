---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329060"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つまたは複数のプロパティ識別子に対応するプロパティ名を提供します。
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a>パラメーター

 _lppproptags_
  
> [入力]入力時に、プロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。それ以外の場合は NULL。すべての名前を返す必要があることを示します。 プロパティタグ配列の**cvalues**メンバーを0にすることはできません。 _lppproptags_が入力に有効なポインターである場合、 **GetNamesFromIDs**は、配列に含まれる各プロパティ識別子の名前を返します。 
    
 _lppropsetguid_
  
> 順番プロパティセットを識別する guid または[guid](guid.md)構造体へのポインター。 _lppropsetguid_パラメーターは、有効なプロパティセットを指すことも、NULL にすることもできます。 
    
 _ulFlags_
  
> 順番返される名前の種類を示すフラグのビットマスク。 次のフラグを使用できます (両方のフラグが設定されている場合、名前は返されません)。
    
MAPI_NO_IDS 
  
> Unicode 文字列として格納されている名前のみを返すように要求します。 
    
MAPI_NO_STRINGS 
  
> 数値識別子として格納されている名前のみを返すように要求します。 
    
 _lpcPropNames_
  
> 読み上げ_lpppropnames_パラメーターによって指定された配列内のプロパティ名ポインターの数へのポインター。 
    
 _lpppPropNames_
  
> 読み上げプロパティ名を含む[mapinameid](mapinameid.md)構造体へのポインターの配列へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティ名が正常に返されました。 
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトは、名前付きプロパティをサポートしていません。 
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、1つ以上のプロパティの名前を返すことができませんでした。 失敗したプロパティのプロパティタグには、 **PT_ERROR**というプロパティの種類があります。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。 
    
MAPI_E_INVALID_PARAMETER 
  
> _lppproptags_によって示されるプロパティタグ配列内の1つ以上のエントリの**cvalues**メンバーが0に設定されています。 
    
## <a name="remarks"></a>解説

ほとんどのプロパティはプロパティ識別子によってアクセスできますが、名前によってアクセスできるプロパティもあります。 **imapiprop:: GetNamesFromIDs**メソッドを呼び出すと、次の操作を実行できます。 
  
- 特定のプロパティセット内の特定のプロパティ識別子の名前を取得します。
    
- 任意のプロパティセット内の特定のプロパティ識別子の名前を取得します。
    
- オブジェクトのマッピングに含まれているすべての名前付きプロパティの名前を取得します。
    
_lppproptags_が1つまたは複数のプロパティ識別子を持つ有効なプロパティタグ配列を指しており、 _lppropsetguid_が有効なプロパティセットをポイントしている場合、 **GetNamesFromIDs**はプロパティセットとプロパティの型を無視し、すべての名前を返します。指定した識別子にマップされます。 
  
_lppproptags_が、1つまたは複数のプロパティ識別子を持つ有効なプロパティタグ配列を指しており、 _lppropsetguid_が NULL の場合、 **GetNamesFromIDs**は指定された識別子にマップされているすべての名前を返します。 
  
指定した識別子に名前が含まれていない場合、 **GetNamesFromIDs**はその識別子が_lpppPropNames_で返される構造内で NULL を返し、MAPI_W_ERRORS_RETURNED も返します。 
  
_lppropsetguid_と_lppproptags_の両方が NULL の場合、 **GetNamesFromIDs**は新しいプロパティタグ配列を割り当て、オブジェクトのすべての名前付きプロパティの名前を返します。 
  
返される名前がない場合は、要求されたプロパティセットにプロパティが存在しないか、またはすべてのプロパティがフラグによって除外される型であるため、 **GetNamesFromIDs**は次の処理を実行します。 
  
- S_OK を返します。
    
- **cvalues**メンバーを0に設定して、新しい**SPropTagArray**構造を割り当てます。 
    
- _lpcPropNames_の内容を0に設定します。 
    
- _lpppPropNames_の内容を NULL に設定します。 
    
## <a name="notes-to-implementers"></a>実装に関するメモ

_lppropsetguid_が有効なプロパティセットを指しており、 _lppproptags_が NULL の場合、結果は未定義となります。 次のいずれかの方法を使用できます。 
  
- プロパティセットを無視し、プロパティタグ配列の識別子の名前を返します。
    
- 指定したプロパティセットに属するプロパティタグ配列内の識別子の名前のみを返します。
    
- 呼び出しを失敗させ、MAPI_E_INVALID_PARAMETER を返します。 
    
## <a name="notes-to-callers"></a>呼び出し側への注意

オブジェクトのすべての名前付きプロパティを取得するには、最初にオブジェクトの[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドを呼び出してから、0x8000 の範囲の上にある返された識別子を**GetNamesFromIDs**に渡します。
  
有効なプロパティセットを渡すが、有効なプロパティタグ配列を渡さない場合は、予期しない結果を得るために準備してください。 **GetNamesFromIDs**の一部の実装では、プロパティセットを無視して、プロパティタグの配列内の識別子の名前を返します。 一部の実装は MAPI_E_INVALID_PARAMETER を返します。 その他の実装では、プロパティセット内のすべてのプロパティの識別子の名前を返します。 プロパティセットが PS_PUBLIC_STRINGS の場合、 **GetNamesFromIDs**は作成されたすべての名前を返すことができます。 パブリック文字列に関連付けられた識別子の下に、サービスプロバイダーがプロパティを格納するかどうかは、immaterial になります。 
  
プロパティ名の指定が終了したら、 _lpcPropNames_パラメーターの内容を確認して、名前が返されたかどうかを確認します。 その場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、正常な結果が返されたときに、 _lppproptags_および_lpppPropNames_が指すメモリを解放します。 **MAPIFreeBuffer**の1回の呼び出しでは、各パラメーターに対して十分です。ポインターの配列をスキャンして、各**mapinameid**構造を個別に解放する必要はありません。 
  
名前付きプロパティの詳細については、「 [MAPI の名前付きプロパティ](mapi-named-properties.md)」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl  <br/> |CSingleMAPIPropListCtrl:: findallnamedprops  <br/> |mfcmapi は、 **imapiprop:: GetNamesFromIDs**メソッドを使用して、以前にマップされていた名前付きプロパティを検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)
  
[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPINAMEID](mapinameid.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)
  
[エラー処理にマクロを使用する](using-macros-for-error-handling.md)


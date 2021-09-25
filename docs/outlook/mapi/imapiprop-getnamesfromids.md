---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b968f76ee5b7f8b76b1ede9d8ce23b363c40e0f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625561"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上のプロパティ識別子に対応するプロパティ名を指定します。
  
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

 _lppPropTags_
  
> [in, out]入力時に、プロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。それ以外の場合は NULL で、すべての名前を返す必要があります。 プロパティ **タグ配列の cValues** メンバーは 0 にすることはできません。 _lppPropTags が_ 入力の有効なポインターである場合 **、GetNamesFromIDs は** 配列に含まれる各プロパティ識別子の名前を返します。 
    
 _lpPropSetGuid_
  
> [in]プロパティ セットを識別する [GUID (GUID](guid.md) 構造) へのポインター。 _lpPropSetGuid_ パラメーターは、有効なプロパティ セットをポイントするか、NULL を指定できます。 
    
 _ulFlags_
  
> [in]返される名前の種類を示すフラグのビットマスク。 次のフラグを使用できます (両方のフラグが設定されている場合、名前は返されません)。
    
MAPI_NO_IDS 
  
> Unicode 文字列として格納されている名前のみを返す要求。 
    
MAPI_NO_STRINGS 
  
> 数値識別子として格納された名前のみを返す要求。 
    
 _lpcPropNames_
  
> [out]  _lppPropNames_ パラメーターが指す配列内のプロパティ名ポインターの数を指すポインター。 
    
 _lpppPropNames_
  
> [out]プロパティ名を含む [MAPINAMEID](mapinameid.md) 構造体へのポインターの配列へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティ名が正常に返されました。 
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトは名前付きプロパティをサポートしていない。 
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、1 つ以上のプロパティの名前を返す必要がありました。 失敗したプロパティのプロパティ タグには、プロパティの種類が **PT_ERROR。** この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。 
    
MAPI_E_INVALID_PARAMETER 
  
> **lppPropTags** が指すプロパティ タグ配列内の 1 つ以上のエントリの _cValues_ メンバーは 0 に設定されます。 
    
## <a name="remarks"></a>注釈

ほとんどのプロパティへのアクセスはプロパティ識別子によって行いますが、一部のプロパティには名前でアクセスできます。 **IMAPIProp::GetNamesFromIDs** メソッドを呼び出して、次の操作を実行できます。 
  
- 特定のプロパティ セット内の特定のプロパティ識別子の名前を取得します。
    
- 任意のプロパティ セット内の特定のプロパティ識別子の名前を取得します。
    
- オブジェクトのマッピングに含まれるすべての名前付きプロパティの名前を取得します。
    
_lppPropTags_ が 1 つ以上のプロパティ識別子を持つ有効なプロパティ タグ配列をポイントし _、lpPropSetGuid_ が有効なプロパティ セットをポイントする場合 **、GetNamesFromIDs** はプロパティ セットとプロパティの種類を無視し、指定された識別子にマップされる名前をすべて返します。 
  
_lppPropTags_ が 1 つ以上のプロパティ識別子を持つ有効なプロパティ タグ配列をポイントし _、lpPropSetGuid_ が NULL の場合 **、GetNamesFromIDs** は、指定された識別子にマップされる名前をすべて返します。 
  
指定した識別子に名前がない場合 **、GetNamesFromIDs** は  _、lpppPropNames_ で返される構造体内のその識別子の場所で NULL を返し、また、その識別子をMAPI_W_ERRORS_RETURNED。 
  
_lpPropSetGuid_ と _lppPropTags_ の両方が NULL の場合 **、GetNamesFromIDs** は新しいプロパティ タグ配列を割り当て、オブジェクトのすべての名前付きプロパティの名前を返します。 
  
要求されたプロパティ セットにプロパティが存在しないか、すべてのプロパティがフラグによって除外された型である場合など、返される名前がない場合 **、GetNamesFromIDs** は次の操作を実行します。 
  
- 値をS_OKします。
    
- 新しい **SPropTagArray** 構造体を割り当て **、cValues** メンバーを 0 に設定します。 
    
- _lpcPropNames の内容を_ 0 に設定します。 
    
- _lpppPropNames の内容を NULL に_ 設定します。 
    
## <a name="notes-to-implementers"></a>実装に関するメモ

_lpPropSetGuid が有効_ なプロパティ セットをポイントし _、lppPropTags_ が NULL の場合、結果は未定義です。 次のいずれかの方法を使用できます。 
  
- プロパティ セットを無視し、プロパティ タグ配列内の識別子の名前を返します。
    
- 指定したプロパティ セットに属するプロパティ タグ配列内の識別子の名前のみを返します。
    
- 呼び出しに失敗し、MAPI_E_INVALID_PARAMETER。 
    
## <a name="notes-to-callers"></a>呼び出し側への注意

オブジェクトのすべての名前付きプロパティを取得するには、まずオブジェクトの [IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドを呼び出してから、0x8000 の範囲を超える返された識別子を **GetNamesFromIDs** に渡す必要があります。
  
有効なプロパティ セットを渡すが、有効なプロパティ タグ配列を渡さない場合は、予期しない結果を得る準備をしてください。 **GetNamesFromIDs** の一部の実装では、プロパティ セットが無視され、プロパティ タグ配列内の識別子の名前が返されます。 一部の実装では、MAPI_E_INVALID_PARAMETER。 それ以外の実装では、プロパティ セット内のすべてのプロパティの識別子の名前が返されます。 プロパティ セットが指定されているPS_PUBLIC_STRINGS **GetNamesFromIDs** は、これまでに作成された名前を返します。 サービス プロバイダーがパブリック文字列に関連付けられた識別子の下にプロパティを格納するかどうかは重要ではありません。 
  
プロパティ名が完成したら  _、lpcPropNames_ パラメーターの内容を確認して、名前が返されたかどうかを確認します。 その場合は [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、成功した結果が返された場合に _lppPropTags と lpppPropNames_ が指すメモリを解放します。  **MAPIFreeBuffer の呼び出しは、パラメーター** ごとに 1 回で十分です。ポインターの配列を走査し、各 **MAPINAMEID** 構造体を個別に解放する必要はない。 
  
名前付きプロパティの詳細については、「MAPI 名前付き [プロパティ」を参照してください](mapi-named-properties.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI は **IMAPIProp::GetNamesFromIDs** メソッドを使用して、以前にマップされた名前付きプロパティを検索します。  <br/> |
   
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


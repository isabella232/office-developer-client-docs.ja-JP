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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a2ec6def319b1f4686a61e9f97a936bfeba0d410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800662"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**適用されます**: Outlook 
  
1 つまたは複数のプロパティの識別子に対応するプロパティ名を提供します。
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a>Parameters

 _lppPropTags_
  
> [で [チェック アウト]プロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインターの入力でそれ以外の場合、NULL の場合、すべての名前が返されることを示します。 プロパティ タグ配列の**あう**メンバーは、0 にすることはできません。 _LppPropTags_が入力時に有効なポインターである場合は、 **GetNamesFromIDs**は、配列に含まれている各プロパティの識別子の名前を返します。 
    
 _lpPropSetGuid_
  
> [in]GUID、または[GUID](guid.md)へのポインター構造体、プロパティ セットを識別します。 _LpPropSetGuid_パラメーターは、有効なプロパティのセットを指すことができますか、NULL にすることができます。 
    
 _ulFlags_
  
> [in]返される名前の種類を示すフラグのビットマスクです。 次のフラグを使用することができます (両方のフラグが設定されている場合の名前は返されません)。
    
MAPI_NO_IDS 
  
> Unicode 文字列として格納されている名前だけが返されるように要求します。 
    
MAPI_NO_STRINGS 
  
> 数字の識別子として保存されている名前だけが返されるように要求します。 
    
 _lpcPropNames_
  
> [out]_LppPropNames_パラメーターが指す配列内のプロパティ名のポインターの数へのポインターです。 
    
 _lpppPropNames_
  
> [out]プロパティ名を格納する[MAPINAMEID](mapinameid.md)構造体へのポインターの配列へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロパティ名が正常に返されました。 
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトは、名前付きプロパティをサポートしていません。 
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは完了しましたが、1 つまたは複数のプロパティの名前は返されませんでした。 **PT_ERROR**のプロパティの型は、障害が発生したプロパティのプロパティ タグであります。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。 
    
MAPI_E_INVALID_PARAMETER 
  
> _LppPropTags_で指定されたプロパティ タグ配列内のエントリの 1 つ以上の**あう**メンバーは 0 に設定されています。 
    
## <a name="remarks"></a>備考

ほとんどのプロパティへのアクセスは、プロパティの識別子では、いくつかのプロパティを名前でアクセスできます。 次の操作には、 **IMAPIProp::GetNamesFromIDs**メソッドを呼び出すことができます。 
  
- 特定のプロパティ セット内の特定のプロパティ識別子の名前を取得します。
    
- 任意のプロパティ セット内の特定のプロパティの識別子の名前を取得します。
    
- オブジェクトのマッピングに含まれるすべての名前付きプロパティの名前を取得します。
    
**GetNamesFromIDs**がプロパティ セットとプロパティの型を無視し、すべての名前を返す 1 つまたは複数のプロパティの識別子を持つ有効なプロパティ タグ配列を指す_lppPropTags_と_lpPropSetGuid_を指す有効なプロパティを設定する場合指定した識別子にマップするとします。 
  
プロパティ識別子と_lpPropSetGuid_の 1 つまたは複数の有効なプロパティ タグ配列を_lppPropTags_ポイントの場合、 **GetNamesFromIDs**を NULL がすべての指定した識別子にマップされる名前を返します。 
  
指定した識別子は、名前を持たない場合、 **GetNamesFromIDs**は_lpppPropNames_で返される構造体でその識別子の場所には NULL を返し、MAPI_W_ERRORS_RETURNED を返します。 
  
_LpPropSetGuid_と_lppPropTags_の両方が NULL の場合、 **GetNamesFromIDs**は新しいプロパティ タグ配列を割り当て、すべてのすべてのオブジェクトの名前付きプロパティの名前を返します。 
  
返される名前がない場合は、おそらく、要求されたプロパティ セットのプロパティはありませんか、フラグで除外された型のすべてのプロパティは、 **GetNamesFromIDs**は、次の。 
  
- S_OK を返します。
    
- **あう**メンバーを 0 に設定する、新しい**SPropTagArray**構造を割り当てます。 
    
- _LpcPropNames_の内容を 0 に設定します。 
    
- _LpppPropNames_の内容を NULL に設定します。 
    
## <a name="notes-to-implementers"></a>実装者へのメモ

_LpPropSetGuid_を指し、有効なプロパティのセット、 _lppPropTags_が NULL の場合、結果は定義されていません。 次の方法のいずれかを使用することができます。 
  
- プロパティの設定を無視し、プロパティ タグ配列の識別子の名前を取得します。
    
- プロパティ タグ配列の指定されたプロパティ セットに属しているだけの識別子の名前を返します。
    
- MAPI_E_INVALID_PARAMETER を返す呼び出しは失敗します。 
    
## <a name="notes-to-callers"></a>呼び出し側への注意

すべてのオブジェクトの名前付きプロパティを取得するには、まずオブジェクトの[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを呼び出すし、 **GetNamesFromIDs**の範囲は 0x8000 を超える返される識別子を渡します。
  
予期しない結果を渡す場合は、有効なプロパティ セットが有効なプロパティ タグの配列ではありません、しておいてください。 **GetNamesFromIDs**の一部の実装では、プロパティの設定を無視し、プロパティ タグ配列の識別子の名前を返します。 いくつかの実装では、MAPI_E_INVALID_PARAMETER を返します。 まだ他の実装では、プロパティ セット内のすべてのプロパティの識別子の名前を返します。 プロパティ セットの PS_PUBLIC_STRINGS 場合、 **GetNamesFromIDs**は、これまでに作成されたすべての名前を返すことができます。 サービス プロバイダーがパブリック文字列に関連付けられている識別子のプロパティを格納するかどうかは、数量単価型ではありません。 
  
プロパティ名を持つが終了したら、任意の名前が返されたかどうかを決定する_lpcPropNames_パラメーターの内容を確認してください。 その場合は、正常な結果が返されるときに_lppPropTags_と_lpppPropNames_が指すメモリを解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 **MAPIFreeBuffer** 1 回の呼び出しはそれぞれのパラメーターに対して十分ですポインターの配列を走査し、各**MAPINAMEID**構造体を個別に解放する必要はありません。 
  
名前付きプロパティの詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI では、 **IMAPIProp::GetNamesFromIDs**メソッドを使用して、以前にマップされている名前付きのプロパティを検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)
  
[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPINAMEID](mapinameid.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)
  
[エラー処理のためのマクロを使用してください。](using-macros-for-error-handling.md)


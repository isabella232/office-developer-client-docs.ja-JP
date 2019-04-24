---
title: imapipropopenproperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319811"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティへのアクセスに使用できるインターフェイスへのポインターを返します。
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>パラメーター

 _ulPropTag_
  
> 順番アクセスされるプロパティのプロパティタグ。 識別子と型の両方が property タグに含まれている必要があります。
    
 _lpiid_
  
> 順番プロパティへのアクセスに使用するインターフェイスの識別子へのポインター。 _lpiid_パラメーターを**null**にすることはできません。
    
 _ulinterfaceoptions_
  
> 順番_lpiid_パラメーターによって識別されるインターフェイスに関連するデータ。 
    
 _ulFlags_
  
> 順番プロパティへのアクセスを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_CREATE 
  
> プロパティが存在しない場合は、作成する必要があります。 プロパティが存在する場合は、プロパティの現在の値を破棄する必要があります。 発信者が MAPI_CREATE フラグを設定する場合は、MAPI_MODIFY フラグも設定する必要があります。
    
MAPI_DEFERRED_ERRORS 
  
> オブジェクトが完全に呼び出し元で使用可能になる前に、 **openproperty**を正常に返すことができるようにします。 オブジェクトが使用できない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。 
    
MAPI_MODIFY 
  
> MAPI_MODIFY は、次のような状況で必要になります。
    
  - stream プロパティ ( **IID_IStream**など) を開いて変更する場合。
    
  - 埋め込みメッセージ添付ファイル ( **IID_IMessage**で開かれた[PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md)など) を開いて変更する場合。
    
 _lppunk_
  
> 読み上げプロパティへのアクセスに使用する要求されたインターフェイスへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 要求されたインターフェイスポインターが正常に返されました。
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> 要求されたインターフェイスは、このプロパティではサポートされていません。
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元に、プロパティにアクセスするための十分な権限がありません。
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトは、要求されたインターフェイス経由でこのプロパティへのアクセスを提供できません。
    
MAPI_E_NOT_FOUND 
  
> 要求されたプロパティが存在せず、 _ulflags_パラメーターに MAPI_CREATE が設定されていません。 
    
MAPI_E_INVALID_PARAMETER 
  
> タグ内のプロパティの型は、PT_UNSPECIFIED に設定されています。
    
## <a name="remarks"></a>解説

**imapiprop:: openproperty**メソッドは、特定のインターフェイスを介してプロパティへのアクセスを提供します。 **openproperty**は、 [imapiprop:: GetProps](imapiprop-getprops.md)および[imapiprop:: setprops](imapiprop-setprops.md)メソッドの代わりになります。 プロパティが大きすぎるか、または複雑すぎるため、 **GetProps**または**setprops**が失敗する場合は、 **openproperty**を呼び出します。 **openproperty**は、通常、PT_OBJECT 型のプロパティにアクセスするために使用されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージの添付ファイルにアクセスするには、添付ファイルの種類に応じて、別のインターフェイス識別子を使用して**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを開きます。 次の表では、さまざまな種類の添付ファイルの**openproperty**を呼び出す方法について説明します。 
  
|**添付ファイルの種類**|**使用するインターフェイス識別子**|
|:-----|:-----|
|Binary  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|メッセージ  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile**は、OLE 2.0 複合ファイルに基づく[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスから派生したものです。 **IStreamDocfile**は、最小限のオーバーヘッドを必要とするため、OLE 2.0 の添付ファイルにアクセスするのに最適です。 IID_IStreamDocFile は、 [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)インターフェイスを介して使用できる構造化ストレージに格納されているデータを含むプロパティに使用できます。 
  
添付ファイル付きの**openproperty**の使用方法の詳細については、 **PR_ATTACH_DATA_OBJ**プロパティを参照し、[添付ファイルを開い](opening-an-attachment.md)てください。
  
0の位置またはサイズ変数を使用しない場合は、受け取った**IStream**ポインターを使用して、 [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx)メソッドまたは[SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx)メソッドを呼び出すことはできません。 また、 **Seek**呼び出しから返される_plibnewposition_出力パラメーターの値に依存しないようにしてください。 
  
**IStream**インターフェイスを使用してプロパティにアクセスするために**openproperty**を呼び出す場合は、そのインターフェイスのみを使用して変更を加えます。 **setprops**や[imapiprop::D eleteprops](imapiprop-deleteprops.md)など、他の[imapiprop: IUnknown](imapipropiunknown.md)メソッドのいずれかを使用してプロパティを更新しないようにしてください。 
  
**openproperty**を持つプロパティを複数回開いてはいけません。 結果は、プロバイダーによって異なる可能性があるため、未定義となります。 
  
開くプロパティを変更する必要がある場合は、MAPI_MODIFY フラグを設定します。 オブジェクトでプロパティがサポートされているかどうかがわからない場合は、MAPI_CREATE フラグと MAPI_MODIFY フラグを設定します。 MAPI_CREATE が設定されている場合は常に、MAPI_MODIFY も設定する必要があります。
  
_lppunk_パラメーターで返されるインターフェイスポインターが、 _lpiid_パラメーターで指定されているインターフェイスに適したものになるように、recasting を担当しています。 また、返されたポインターを使用して、終了時に[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出す必要があります。 
  
_ulflags_パラメーターのフラグを設定しても、必要なプロパティへのアクセスの種類を示すには不十分な場合があります。 _ulinterfaceoptions_パラメーターには、フラグなどの追加データを入れることができます。 このデータはインターフェイスに依存します。 **IStream**などの一部のインターフェイスは、それを使用します。そうでないものもあります。 たとえば、 **IStream**を使用して変更するプロパティを開いた場合は、MAPI_MODIFY に加えて、 _ulinterfaceoptions_パラメーターの STGM_WRITE フラグを設定します。 [IMAPITable](imapitableiunknown.md)インターフェイスを使用してテーブルを開いた場合、MAPI_UNICODE に_ulinterfaceoptions_を設定して、テーブル内の文字列プロパティを保持する列が UNICODE 形式であるかどうかを示すことができます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|streameditor .cpp  <br/> |cstreameditor:: readtextstreamfromproperty  <br/> |mfcmapi は、 **imapiprop:: openproperty**メソッドを使用して、大きなテキストおよびバイナリプロパティのストリームインターフェイスを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)
- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
- [添付ファイルを開く](opening-an-attachment.md)


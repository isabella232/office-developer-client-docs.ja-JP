---
title: IMAPIPropOpenProperty
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 656e5c5532edfc6c791ca30aa30f4c4d96847295
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800661"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**適用されます**: Outlook 
  
プロパティにアクセスするために使用するインターフェイスへのポインターを返します。
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _ulPropTag_
  
> [in]アクセスするプロパティのプロパティ タグです。 識別子と型の両方は、プロパティ タグに含める必要があります。
    
 _lpiid_
  
> [in]プロパティへのアクセスに使用するインターフェイスの識別子へのポインター。 _Lpiid_パラメーターを**null**にするにはできません。
    
 _ulInterfaceOptions_
  
> [in]_Lpiid_パラメーターで識別されるインターフェイスに関連するデータです。 
    
 _ulFlags_
  
> [in]プロパティへのアクセスを制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
タグ 
  
> プロパティが存在しない場合は作成する必要があります。 プロパティが存在する場合、プロパティの現在の値は破棄されます。 タグ フラグを設定すると、呼び出し元としても、MAPI_MODIFY フラグを設定する必要があります。
    
MAPI_DEFERRED_ERRORS 
  
> 正常に戻す、可能性のあるオブジェクトが呼び出し元に完全に利用できる前に**OpenProperty**を使用できます。 オブジェクトが使用できない場合は、後続のオブジェクトの呼び出しを行うとエラーが発生します。 
    
MAPI_MODIFY 
  
> MAPI_MODIFY がこのような状況で必要です。
    
  - 時、 **IID_IStream**、それを変更するなどのストリームのプロパティを開いています。
    
  - 時、 [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md)を**IID_IMessage**、それを変更すると開くように、埋め込みメッセージの添付ファイルを開いています。
    
 _lppUnk_
  
> [out]プロパティへのアクセスに使用する要求されたインターフェイスへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 要求されたインターフェイス ポインターが正常に返されました。
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> このプロパティには、要求されたインターフェイスはサポートされていません。
    
MAPI_E_NO_ACCESS 
  
> 呼び出し側では、プロパティにアクセスする十分なアクセス許可を持っています。
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトは、要求されたインターフェイスには、このプロパティへのアクセスを提供できません。
    
MAPI_E_NOT_FOUND 
  
> 要求されたプロパティが存在しないため、 _ulFlags_パラメーターのタグが設定されていませんでした。 
    
MAPI_E_INVALID_PARAMETER 
  
> タグのプロパティの型は、PT_UNSPECIFIED に設定されます。
    
## <a name="remarks"></a>備考

**IMAPIProp::OpenProperty**メソッドは、特定のインターフェイスからプロパティへのアクセスを提供します。 **OpenProperty**は、 [IMAPIProp::GetProps](imapiprop-getprops.md)と[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドの代替です。 **GetProps**または**SetProps**のいずれかのプロパティには、大きすぎる、または複雑すぎるために失敗した場合、 **OpenProperty**を呼び出します。 **OpenProperty**は、PT_OBJECT の種類のプロパティにアクセスするのには通常使用されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージの添付ファイルにアクセスするには、添付ファイルの種類に応じて、別のインターフェイス識別子を使用して**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) のプロパティを開きます。 次の表には、さまざまな種類の添付ファイルの**OpenProperty**を呼び出す方法について説明します。 
  
|**添付ファイルの種類**|**インターフェイス識別子を使用するには**|
|:-----|:-----|
|バイナリ型 (Binary)  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Message  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile**は、OLE 2.0 の複合ファイルに基づく[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスの派生物です。 **IStreamDocfile**は、最小限のオーバーヘッドが伴うので、OLE 2.0 の添付ファイルをアクセスするための最適な選択肢です。 [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx)インターフェイスを使用できるが構造化ストレージに保存されたデータが含まれているこれらのプロパティには、IID_IStreamDocFile を使用できます。 
  
添付ファイル付きの**OpenProperty**を使用する方法の詳細については、 **PR_ATTACH_DATA_OBJ**プロパティと[添付ファイルを開く](opening-an-attachment.md)を参照してください。
  
メソッドを呼び出すときに、[シーク](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx)または[setsize 関数](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx)のいずれか、ゼロの位置またはサイズの変数を使用する場合を除き、受信した**IStream**ポインターを使用しません。 **シーク**の呼び出しから返された_plibNewPosition_の出力パラメーターの値に依存しないでも、します。 
  
**IStream**インターフェイスを使用してプロパティにアクセスするのには**OpenProperty**を呼び出す場合は、変更することをそのインタ フェースを使用します。 その他のプロパティを更新しようとはしないで[IMAPIProp: IUnknown](imapipropiunknown.md) **SetProps**や[IMAPIProp::DeleteProps](imapiprop-deleteprops.md)などのメソッドです。 
  
**OpenProperty**のプロパティを複数回開くしないでください。 プロバイダーによって異なる場合があるため、結果は定義されていません。 
  
開く] プロパティを変更する場合は、MAPI_MODIFY フラグを設定します。 オブジェクトがプロパティをサポートするかどうかがわからない場合は、必要と思われるタグと MAPI_MODIFY フラグを設定します。 タグを設定すると、MAPI_MODIFY も設定する必要があります。
  
_Lpiid_パラメーターで指定されたインターフェイスに対応する 1 つに、 _lppUnk_パラメーターで返されるインターフェイス ポインターを見直すために責任があります。 メソッドを呼び出す[が](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)操作を終了するときに返されたポインターを使用することもする必要があります。 
  
_UlFlags_パラメーターでフラグを設定ことがあります不足のために必要なプロパティへのアクセスの種類を示すためにではありません。 _UlInterfaceOptions_パラメーターには、フラグなどの追加データを配置できます。 依存するインターフェイスです。 いくつかのインタ フェース ( **IStream**) が使われ、そうでないです。 たとえば、 **IStream**を変更するプロパティを開くと MAPI_MODIFY だけでなく、 _ulInterfaceOptions_パラメーターに STGM_WRITE フラグを設定します。 [IMAPITable](imapitableiunknown.md)インターフェイスを使用してテーブルを開くときは、文字列のプロパティを保持するテーブルの列が Unicode 形式である必要があるかどうかを示すために MAPI_UNICODE に_ulInterfaceOptions_を設定できます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI では、 **IMAPIProp::OpenProperty**メソッドを使用して、サイズの大きなテキストおよびバイナリのプロパティのストリーム インターフェイスを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable: IUnknown](imapitableiunknown.md)
- [IMAPIProp: IUnknown](imapipropiunknown.md)
- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
- [添付ファイルを開く](opening-an-attachment.md)


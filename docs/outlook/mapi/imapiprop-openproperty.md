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
description: '最終更新日: 2015 年 3 月 9 日'
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
  
> [in]アクセスするプロパティのプロパティ タグ。 識別子と型の両方をプロパティ タグに含める必要があります。
    
 _lpiid_
  
> [in]プロパティへのアクセスに使用するインターフェイスの識別子へのポインター。 _lpiid パラメーターは_ null に **することはできません**。
    
 _ulInterfaceOptions_
  
> [in]  _lpiid_ パラメーターで識別されるインターフェイスに関連するデータ。 
    
 _ulFlags_
  
> [in]プロパティへのアクセスを制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_CREATE 
  
> プロパティが存在しない場合は、作成する必要があります。 プロパティが存在する場合は、プロパティの現在の値を破棄する必要があります。 呼び出し元が MAPI_CREATEフラグを設定すると、呼び出し元フラグMAPI_MODIFYする必要があります。
    
MAPI_DEFERRED_ERRORS 
  
> オブジェクトが呼び出し元で完全に使用できる前に **、OpenProperty** が正常に返されるのを許可します。 オブジェクトを使用できない場合は、後続のオブジェクト呼び出しでエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> MAPI_MODIFYは、次の状況で必要です。
    
  - ストリーム プロパティを開く場合 **(IID_IStreamなど)** を変更します。
    
  - 埋め込みメッセージ添付ファイルを開く場合 (PR_ATTACH_DATA_OBJ [で開](pidtagattachdataobject-canonical-property.md) IID_IMessage **など)** を変更します。
    
 _lppUnk_
  
> [out]プロパティ アクセスに使用する要求されたインターフェイスへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 要求されたインターフェイス ポインターが正常に返されました。
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> 要求されたインターフェイスは、このプロパティではサポートされていません。
    
MAPI_E_NO_ACCESS 
  
> 呼び出し元には、プロパティにアクセスするためのアクセス許可が不十分です。
    
MAPI_E_NO_SUPPORT 
  
> オブジェクトは、要求されたインターフェイスを介してこのプロパティへのアクセスを提供できません。
    
MAPI_E_NOT_FOUND 
  
> 要求されたプロパティは存在し  _MAPI_CREATE ulFlags パラメーターに設定_ されません。 
    
MAPI_E_INVALID_PARAMETER 
  
> タグ内のプロパティの種類は、プロパティの種類にPT_UNSPECIFIED。
    
## <a name="remarks"></a>注釈

**IMAPIProp::OpenProperty** メソッドは、特定のインターフェイスを介してプロパティにアクセスできます。 **OpenProperty は**[、IMAPIProp::GetProps](imapiprop-getprops.md)メソッドと [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドの代替手段です。 プロパティが **大きすぎる** か複雑すぎるため **、GetProps または SetProps** が失敗した場合は **、OpenProperty を呼び出します**。 **OpenProperty は** 、通常、型のプロパティにアクセスするために使用PT_OBJECT。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージの添付ファイルにアクセスするには、添付 **PR_ATTACH_DATA_OBJ** の種類に応じて、異なるインターフェイス識別子を持つ PR_ATTACH_DATA_OBJ ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを開きます。 次の表では、さまざまな種類の添付ファイルに対して **OpenProperty** を呼び出す方法について説明します。 
  
|**添付ファイルの種類**|**使用するインターフェイス識別子**|
|:-----|:-----|
|バイナリ  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|メッセージ  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** は、OLE 2.0 複合ファイルに基づく [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) インターフェイスの派生物です。 **IStreamDocfile は** 、オーバーヘッドが最も少ないので、OLE 2.0 添付ファイルにアクセスするための最適な選択肢です。 [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)インターフェイスIID_IStreamDocFile使用できる構造化ストレージに格納されているデータを含むプロパティには、このプロパティを使用できます。 
  
添付ファイルで **OpenProperty** を使用する方法の詳細については、「PR_ATTACH_DATA_OBJ」および「添付 **ファイルを開** く [」を参照してください](opening-an-attachment.md)。
  
0 の位置またはサイズ変数を使用しない限り、[](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx)受け取った **IStream** ポインターを使用して Seek メソッドまたは [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx)メソッドを呼び出さません。 また **、Seek** 呼び出しから返される _plibNewPosition_ 出力パラメーターの値に依存しない。 
  
**OpenProperty を呼び出** して **IStream** インターフェイスを使用してプロパティにアクセスする場合は、そのインターフェイスのみを使用して変更を加えます。 **SetProps** や [IMAPIProp::D eleteProps](imapiprop-deleteprops.md)など、他の [IMAPIProp : IUnknown](imapipropiunknown.md)メソッドを使用してプロパティを更新しようとはしない。 
  
**OpenProperty** を使用してプロパティを 2 回以上開かれません。 結果はプロバイダーによって異なることがありますので、未定義です。 
  
開くプロパティを変更する必要がある場合は、プロパティフラグをMAPI_MODIFYします。 オブジェクトがプロパティをサポートするかどうかが分からず、必要と思う場合は、プロパティフラグとMAPI_CREATE設定MAPI_MODIFYしてください。 設定されているMAPI_CREATE、MAPI_MODIFY設定する必要があります。
  
_lppUnk_ パラメーターで返されるインターフェイス ポインターを、lpiid パラメーターで指定されたインターフェイスに適したインターフェイス ポインターに再キャストする _必要_ があります。 返されたポインターを使用して、終了したら [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) メソッドを呼び出す必要があります。 
  
_ulFlags_ パラメーターでフラグを設定すると、必要なプロパティへのアクセスの種類を示すのに十分ではない場合があります。 _ulInterfaceOptions_ パラメーターには、フラグなどの追加のデータを設定できます。 このデータはインターフェイスに依存します。 一部のインターフェイス **(IStream** など) が使用し、使用しないインターフェイスもあります。 たとえば **、IStream** を使用して変更するプロパティを開く場合は、STGM_WRITE フラグに加えて  _ulInterfaceOptions_ パラメーター MAPI_MODIFY。 [IMAPITable](imapitableiunknown.md)インターフェイスを使用してテーブルを開く場合は _、ulInterfaceOptions_ を MAPI_UNICODE に設定して、文字列プロパティを保持するテーブル内の列を Unicode 形式にするかどうかを指定できます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI は **IMAPIProp::OpenProperty** メソッドを使用して、大きなテキストおよびバイナリ プロパティのストリーム インターフェイスを取得します。  <br/> |
   
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


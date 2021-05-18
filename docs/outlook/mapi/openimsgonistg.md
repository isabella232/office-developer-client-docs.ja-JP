---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406522"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ セッション内で使用する、既存の OLE **IStorage** オブジェクトの上に新しい [IMessage](imessageimapiprop.md)オブジェクトを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a>パラメーター

_lpMsgSess_
  
> [in]新しい **IMessage**-on- **IStorage** オブジェクトを作成するメッセージ セッション オブジェクトへのポインター。 
    
_lpAllocateBuffer_
  
> [in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。 
    
_lpAllocateMore_
  
> [in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。 
    
_lpFreeBuffer_
  
> [in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。 
    
_lpMalloc_
  
> [in]OLE **IMalloc** インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。 **IMessage インターフェイスは****、IStorage** や IStream などのインターフェイスを操作するときに、この割り当て方法を使用 **する必要があります**。 
    
_lpMapiSup_
  
> [in]サービス プロバイダーが [IMAPISupport : IUnknown](imapisupportiunknown.md) インターフェイスのメソッドを呼び出す場合に使用できる MAPI サポート オブジェクトへのオプションのポインター。 
    
_lpStg_
  
> [in, out]開いている、読 **み取り専用** または読み取り/書き込みアクセス許可を持つ OLE IStorage オブジェクトへのポインター。 **IMessage は書** き込み専用アクセスをサポートしないので **、OpenIMsgOnIStg** は書き込み専用モードで開いたストレージ オブジェクトを受け入れません。 
    
_lpfMsgCallRelease_
  
> [in]**IMessage**-on- **IStorage** オブジェクトの最後のリリースに従って MAPI が呼び出す [MSGCALLRELEASE](msgcallrelease.md)プロトタイプに基づくコールバック関数へのオプションのポインター。 
    
_ulCallerData_
  
> [in] **IMessage**-on- **IStorage** オブジェクトを使用して MAPI によって保存され **、MSGCALLRELEASE** ベースのコールバック関数に渡された呼び出し元データ。 データは、リリースされる **IMessage** オブジェクトと、その上に作成された **IStorage** オブジェクトに関するコンテキストを提供します。 
    
_ulFlags_
  
> [in]クライアント アプリケーションまたはサービス プロバイダーが **IMessage::SaveChanges** メソッドを呼び出す場合に OLE **IStorage::Commit** メソッドを呼び出すかどうかを制御するために使用されるフラグのビットマスク。 次のフラグを設定できます。 
    
IMSG_NO_ISTG_COMMIT 
  
> OLE メソッド **IStorage::Commit** は、クライアントまたはプロバイダーが SaveChanges を呼び出す場合は呼 [び出されません](imapiprop-savechanges.md)。 
    
MAPI_UNICODE
  
> Unicode .msg ファイルの作成を有効にする。 結果の [IMessage](imessageimapiprop.md) ファイルは、そのSTORE_UNICODE_OKにPR_STORE_SUPPORT_MASK [Unicode](pidtagstoresupportmask-canonical-property.md) プロパティをサポートします。 
    
  > [!NOTE]
  > このMAPI_UNICODEフラグは、2003 以上のOutlookでのみサポートされます。 
  
_lppMsg_
  
> [out]開いた **IMessage** オブジェクトへのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

プロパティ属性にアクセスできるのは、プロパティ オブジェクト、つまり [IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスを実装するオブジェクトのみです。 OLE 構造化ストレージ オブジェクトで MAPI プロパティを使用するために **、OpenIMsgOnIStg** は OLE **IStorage** オブジェクトの上に [IMessage : IMAPIProp](imessageimapiprop.md)オブジェクトを作成します。 このようなオブジェクトのプロパティ属性は [、SetAttribIMsgOnIStg](setattribimsgonistg.md) を使用して設定または変更し [、GetAttribIMsgOnIStg](getattribimsgonistg.md)を使用して取得できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**OpenIMsgOnIStg** が呼び出される前に [、OpenIMsgSession](openimsgsession.md)でメッセージ セッションを開く必要があります。 有効な  _lpMsgSess_ パラメーターを指定すると、新しいメッセージがメッセージ セッション内に作成され、セッションが閉じられます。 _lpMsgSess が_ NULL の場合、メッセージはメッセージ セッションとは別に作成されます。 メッセージを作成したクライアント アプリケーションまたはサービス プロバイダーが、メッセージを解放しない場合、添付ファイルと開いているテーブルのすべてが解放されない場合、メモリがリークされ、アプリケーションが終了する可能性があります。 
  
MAPI では、ほとんどのメモリ割り当ておよび割り当て解除に _lpAllocateBuffer_ _、lpAllocateMore、lpFreeBuffer_ が指す関数を使用して、特に [IMAPIProp::GetProps](imapiprop-getprops.md)や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際にクライアント アプリケーションで使用するメモリを割り当てる。  **OpenIMsgOnIStg** 関数が有効な _lpMapiSup_ パラメーターで呼び出される場合 _、lpAllocateBuffer_ _、lpAllocateMore、_ および _lpFreeBuffer_ ポインターはオプションです。 
  
基になる OLE オブジェクトを扱うので、MAPI では OLE メモリ割り当てを使用する必要があります。 OLE 構造化ストレージ オブジェクトと OLE メモリ割り当ての詳細については  _、「OLE プログラマリファレンス」を参照してください_。 
  
_lpMapiSup_ に対して有効な値が指定されている場合 **、IMessage** は [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出して [IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドと [IMessage::D eleteAttach](imessage-deleteattach.md)メソッドの進行状況ユーザー インターフェイスを指定することで、MAPI_DIALOG フラグと ATTACH_DIALOG フラグをサポートします。 [また、IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドは[、IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md)メソッドを呼び出し、結果のアドレス帳オブジェクトを呼び出すことによって、短期エントリ識別子を長期エントリ識別子に変換します。 _lpMapiSup_ に NULL が渡された場合 **、IMessage** は MAPI_DIALOG および ATTACH_DIALOG を無視し、変換なしで短期エントリ識別子を格納します。 
  
**lpStg パラメーターが** 指す _IStorage_ オブジェクトは、STGM_READモードSTGM_READWRITEがあります。 このモードSTGM_READWRITE場合は、STGM_TRANSACTEDモードも設定する必要があります。 
  
_lpfMsgCallRelease_ パラメーターが指すコールバック関数はオプションです。指定されている場合は [、MSGCALLRELEASE 関数プロトタイプに基づく](msgcallrelease.md)必要があります。 **IMessage** インターフェイスは **、IMessage**-on- **IStorage** オブジェクトの参照カウントが Release メソッドの最後の呼び出しによって 0 に設定されている場合に呼び **出** します。 コールバック関数は、基になる **IStorage** インターフェイスを解放するために一般的に使用されます。 **IMessage** は、コールバックを行った後 _、lpStg_ パラメーターが指す **IStorage** オブジェクトにアクセスしようとは行ないます。 
  
一部のクライアントまたはプロバイダーは [、SaveChanges](imapiprop-savechanges.md)メソッドの呼び出し時に IMessage 自体が書き込むデータを超えて **、IStorage** オブジェクトに追加のデータを書き込む場合があります。  クライアントまたはプロバイダーは、IMSG_NO_ISTG_COMMIT フラグを使用して **、SaveChanges** 呼び出しの処理中に **IMessage** が OLE **IStorage::Commit** メソッドを呼び出すのを防止できます。この場合、クライアントまたはプロバイダーは、追加のデータの書き込み時に **IStorage** オブジェクトをコミットする必要があります。 これを支援するために **、IMessage** 実装では **、IStorage** オブジェクトで作成するサブストルジの名前は、文字列 "__"、つまり 2 つのアンダースコアで始まります。 クライアントまたはプロバイダーは、サブストラージュ名をこの名前空間から外して名前の競合を回避できます。 
  
MAPI は、添付ファイル、ストリーム、埋め込みメッセージなど、メッセージのサブオブジェクトに対して実行される複数の開いている操作の動作を定義しません。 MAPI は現在、既に開いているサブオブジェクトをもう一度開くことを許可していますが、MAPI は、既存の開いているオブジェクトの参照カウントを増やし [、IMessage::OpenAttach](imessage-openattach.md) メソッドまたは [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出したクライアントまたはプロバイダーに返して、開いている操作を実行します。 つまり、サブオブジェクトの最初の開いている操作に対して要求されたアクセスは、操作によって要求されたアクセスに関係なく、後続のすべての開いている操作に対して提供されるアクセスです。 
  
メッセージを添付ファイルに配置する正しい手順は [、IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出し、インターフェイス識別子を使用して IID_IMessage。 **OpenProperty は** 現在、OLE **IStorage** インターフェイスで直接使用できるメッセージ添付ファイルの作成 (つまり、このインターフェイス識別子を使用IID_IStorageサポートしています。 **IStorage** アクセスは、OLE IStream インターフェイスに変換したり、OLE **IStream** インターフェイスから変換したりすることなく、Microsoft Word ドキュメントを添付ファイルに簡単に挿入するためのサポートされています。 ただし **、OpenIMsgOnIStg** が添付ファイル データに **IStorage** ポインターを渡され、オブジェクトが間違った順序で解放された場合 **、IMessage** は予測可能に動作しない可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI は **OpenIMsgOnIStg** メソッドを使用して、 の上に IMessage インターフェイスを開きます。ファイルが MAPI で操作される可能性がある MSG ファイル。  <br/> |
   
## <a name="see-also"></a>関連項目

- [�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)


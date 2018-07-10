---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 127c4a77b9184d8bb62925c5237c1aedec643992
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801699"
---
# <a name="openstreamonfilew"></a>OpenStreamOnFileW

  
  
**適用されます**: Outlook 
  
ファイルの内容にアクセスするのには OLE **IStream**オブジェクトを初期化します。 この関数は、UNICODE 文字列は、引数、 [OpenStreamOnFile](openstreamonfile.md)関数の ANSI バージョンとは異なり、できるので、パスとファイル拡張子を含むファイル名に任意の文字の。
  
|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |olmapi32.dll  <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameters

 _lpAllocateBuffer_
  
> [in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _ulFlags_
  
> [in]OLE **IStream**オブジェクトを通じてアクセスするのファイルを開くまたは作成を制御するために使用するフラグのビットマスクです。 次のフラグを設定することができます。 
    
SOF_UNIQUEFILENAME
  
> 一時ファイルは、 **IStream**オブジェクトを作成するのには。 このフラグが設定されている場合、STGM_CREATE と STGM_READWRITE のフラグも設定してください。 
    
STGM_CREATE
  
> ファイルは、1 つ既に存在する場合でも作成すること。 _場合_パラメーターが設定されていない場合は、このフラグと STGM_DELETEONRELEASE の両方を設定する必要があります。 STGM_CREATE が設定されている場合、STGM_READWRITE のフラグも設定する必要があります。 
    
STGM_DELETEONRELEASE
  
> ファイルでは、 **IStream**オブジェクトが解放されるときに削除されます。 _場合_パラメーターが設定されていない場合は、このフラグと STGM_CREATE の両方を設定する必要があります。 
    
STGM_READ
  
> ファイルは読み取り専用アクセスで開くまたは作成するのには。
    
STGM_READWRITE
  
> ファイルは、読み取り/書き込み権限で開くまたは作成するのには。 このフラグが設定されていない場合、STGM_CREATE フラグする必要がありますを設定できませんか。
    
 _場合_
  
> [in]ファイル名、パスと、Unicode の拡張子を含む**IStream**オブジェクトを初期化する**OpenStreamOnFileW**のファイルの名前です。 SOF_UNIQUEFILENAME フラグが設定されている場合、_場合_に、一時ファイルを作成するためのディレクトリへのパスが含まれています。 _場合_が NULL の場合は、 **OpenStreamOnFileW**は、システムから適切なパスを取得し、STGM_CREATE と STGM_DELETEONRELEASE の両方のフラグを設定する必要があります。 
    
 _lpszPrefix_
  
> [in]Unicode ファイル名を**OpenStreamOnFileW**が、 **IStream**オブジェクトを初期化するためのプレフィックス。 かどうか設定すると、プレフィックスする必要がありますが含まれている以下の 3 文字です。 _LpszPrefix_が NULL の場合は、"SOF"の接頭辞を使用します。 
    
 _lppStream_
  
> [out]**IStream**インターフェイスを公開するオブジェクトへのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_ACCESS
  
> 権限のないユーザーがファイルにアクセスできませんでしたか、読み取り専用ファイルを変更できないためです。
    
MAPI_E_NOT_FOUND
  
> 指定のファイルが存在しません。
    
## <a name="remarks"></a>備考

**OpenStreamOnFileW**関数では、SOF_UNIQUEFILENAME フラグの設定によって、Unicode 名を持つファイルの他の 2 つの重要な用途があります。 **OpenStreamOnFileW**が**IStream**オブジェクトの例では、 **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) のプロパティに、**を使用して添付ファイルの内容をコピーするのには、既存のファイルを開きますこのフラグが設定されていない場合IStream::CopyTo**メソッドです。 ここで_場合_のパラメーターは、ファイルのファイル名とパスを指定します。 
  
SOF_UNIQUEFILENAME を設定すると、 **OpenStreamOnFileW**は、 **IStream**オブジェクトのデータを保持する一時ファイルを作成します。 この使用方法の_場合_のパラメーターはオプションで、ファイルを作成するのには、 _lpszPrefix_パラメーターは、ファイル名のプレフィックスをオプションで指定できます、ディレクトリへのパスを指定できます。 
  
**IStream**オブジェクトには、呼び出し元のクライアント アプリケーションまたはサービス プロバイダーが終了したらは、OLE **IStream::Release**メソッドを呼び出すことによって解放にする必要があります。 
  
MAPI で示される_lpAllocateBuffer_および多くのメモリの割り当てと解放の_lpFreeBuffer_特に[IMAPIProp などのオブジェクトのインターフェイスを呼び出すときに、クライアント アプリケーションによって使用するメモリを割り当てることの機能を使用します。GetProps](imapiprop-getprops.md)と[IMAPITable::QueryRows](imapitable-queryrows.md)。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージング システムに固有の名前を持つ一時ファイルを作成するのには SOF_UNIQUEFILENAME フラグを使用します。 このフラグが設定されている場合、一時ファイルと_lpszPrefix_パラメーターのパスである_場合_のパラメーターを指定には、ファイル名の先頭の文字が含まれています。 構築されたファイル名は<prefix>HHHH。TMP は 16 進数です。 _場合_が NULL の場合は、ファイルは**値**では、Windows の機能から返される一時ファイルのディレクトリまたは現在のディレクトリに一時ファイルのディレクトリが指定されていない場合。
  
SOF_UNIQUEFILENAME フラグが設定されていない場合は、 _lpszPrefix_は無視され、_場合_は、開くまたは作成するファイルのファイル名と完全修飾パスを含める必要があります。 ファイルを開くか_ulFlags_に設定されている他のフラグを基に作成されます。
  
## <a name="see-also"></a>関連項目



[OpenStreamOnFile](openstreamonfile.md)

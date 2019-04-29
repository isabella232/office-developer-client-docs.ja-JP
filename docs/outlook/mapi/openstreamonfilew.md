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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406025"
---
# <a name="openstreamonfilew"></a>OpenStreamOnFileW

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
OLE **IStream**オブジェクトを割り当てて初期化し、ファイルの内容にアクセスします。 この関数は、UNICODE 文字列を引数として受け取ります。この関数[openstreamonfile](openstreamonfile.md)の ANSI バージョンとは異なり、パスとファイル拡張子を含むファイル名には任意の文字を使用できます。
  
|||
|:-----|:-----|
|エクスポート対象:  <br/> |olmapi32  <br/> |
|実装元:  <br/> |Outlook  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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

## <a name="parameters"></a>パラメーター

 _lpAllocateBuffer_
  
> 順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpfreebuffer_
  
> 順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _ulFlags_
  
> 順番OLE **IStream**オブジェクトを通じてアクセスされるファイルの作成またはオープンを制御するために使用されるフラグのビットマスクです。 次のフラグを設定できます。 
    
SOF_UNIQUEFILENAME
  
> **IStream**オブジェクトの一時ファイルが作成されます。 このフラグが設定されている場合は、STGM_CREATE と STGM_READWRITE のフラグも設定する必要があります。 
    
STGM_CREATE
  
> ファイルは、既に存在している場合でも作成されます。 _lpszfilename_パラメーターが設定されていない場合は、このフラグと STGM_DELETEONRELEASE の両方を設定する必要があります。 STGM_CREATE が設定されている場合は、STGM_READWRITE フラグも設定する必要があります。 
    
STGM_DELETEONRELEASE
  
> **IStream**オブジェクトが解放されるときに、ファイルを削除します。 _lpszfilename_パラメーターが設定されていない場合は、このフラグと STGM_CREATE の両方を設定する必要があります。 
    
STGM_READ
  
> ファイルを作成するか、読み取り専用アクセスで開くかを指定します。
    
STGM_READWRITE
  
> ファイルは読み取り/書き込みアクセス許可で作成または開くことができます。 このフラグが設定されていない場合は、STGM_CREATE フラグを設定しないでください。
    
 _lpszfilename_
  
> 順番**openstreamonfilew**が**IStream**オブジェクトを初期化する、Unicode 名前付きファイルのパスと拡張子を含むファイル名。 SOF_UNIQUEFILENAME フラグが設定されている場合、 _lpszfilename_には、一時ファイルを作成するディレクトリへのパスが含まれます。 _lpszfilename_が NULL の場合、 **openstreamonfilew**はシステムから適切なパスを取得し、STGM_CREATE と STGM_DELETEONRELEASE の両方のフラグを設定する必要があります。 
    
 _lpszprefix_
  
> 順番**openstreamonfilew**が**IStream**オブジェクトを初期化する Unicode ファイル名のプレフィックス。 設定されている場合、プレフィックスは3文字以下である必要があります。 _lpszprefix_が NULL の場合は、プレフィックス "SOF" が使用されます。 
    
 _lppstream_
  
> 読み上げ**IStream**インターフェイスを公開しているオブジェクトへのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_ACCESS
  
> ユーザーのアクセス許可が不足しているため、または読み取り専用ファイルを変更できないため、ファイルにアクセスできませんでした。
    
MAPI_E_NOT_FOUND
  
> 指定したファイルが存在しません。
    
## <a name="remarks"></a>注釈

**openstreamonfilew**関数には、SOF_UNIQUEFILENAME フラグの設定によって区別された Unicode 名を持つファイルの処理に加えて、2つの重要な機能があります。 このフラグが設定されていない場合、 **openstreamonfilew** **** は**** [](pidtagattachdatabinary-canonical-property.md)**既存のファイルに IStream オブジェクトを開きます。たとえば、コンテンツを添付ファイルの PR_ATTACH_DATA_BIN (PidTagAttachDataBinary) プロパティにコピーします。IStream:: CopyTo**メソッド。 この場合、 _lpszfilename_パラメーターには、ファイルのパスとファイル名を指定します。 
  
SOF_UNIQUEFILENAME が設定されている場合、 **openstreamonfilew**は、 **IStream**オブジェクトのデータを保持するための一時ファイルを作成します。 この使用法では、必要に応じて、ファイルを作成するディレクトリへのパスを_lpszfilename_パラメーターで指定できます。また、必要に応じて、 _lpszfilename_パラメーターでファイル名のプレフィックスを指定することもできます。 
  
呼び出し元クライアントアプリケーションまたはサービスプロバイダーが**IStream**オブジェクトで終了すると、OLE **istream:: Release**メソッドを呼び出して解放する必要があります。 
  
MAPI では、特に、 _lpAllocateBuffer_および_lpfreebuffer_で参照されている関数を使用して、imapiprop などのオブジェクトインターフェイスを呼び出すときに、クライアントアプリケーションが使用するメモリを割り当て[ます。GetProps](imapiprop-getprops.md)と[IMAPITable:: QueryRows](imapitable-queryrows.md)。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

SOF_UNIQUEFILENAME フラグは、メッセージングシステムに固有の名前を持つ一時ファイルを作成するために使用されます。 このフラグが設定されている場合、 _lpszfilename_パラメーターは一時ファイルのパスを指定し、 _lpszfilename_パラメーターにはファイル名の先頭文字が含まれます。 構築された<prefix>ファイル名は hhhhhhhh-hhhh-hhhh-hhhh-hhhhhhhhhhhh です。TMP、hhhhhhhh-hhhh-hhhh-hhhh-hhhhhhhhhhhh は16進数の数値です。 _lpszfilename_が NULL の場合は、Windows 関数**GetTempPath**から返される一時ファイルディレクトリ、または一時ファイルディレクトリが指定されていない場合は現在のディレクトリにファイルが作成されます。
  
SOF_UNIQUEFILENAME フラグが設定されていない場合、 _lpszprefix_は無視され、 _lpszprefix_には開くまたは作成するファイルの完全修飾パスとファイル名が含まれている必要があります。 このファイルは、 _ulflags_に設定されている他のフラグに基づいて開かれるか作成されます。
  
## <a name="see-also"></a>関連項目



[OpenStreamOnFile](openstreamonfile.md)


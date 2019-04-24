---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348630"
---
# <a name="openstreamonfile"></a><span data-ttu-id="090e6-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="090e6-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="090e6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="090e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="090e6-105">OLE **IStream**オブジェクトを割り当てて初期化し、ファイルの内容にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="090e6-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="090e6-106">この関数は、パスとファイル拡張子を含むファイル名として ANSI 文字列を受け取ります。このため、 [openstreamonfilew](openstreamonfilew.md)の Unicode バージョンを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="090e6-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="090e6-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="090e6-107">Header file:</span></span>  <br/> |<span data-ttu-id="090e6-108">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="090e6-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="090e6-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="090e6-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="090e6-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="090e6-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="090e6-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="090e6-111">Called by:</span></span>  <br/> |<span data-ttu-id="090e6-112">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="090e6-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="090e6-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="090e6-113">Parameters</span></span>

 <span data-ttu-id="090e6-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="090e6-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="090e6-115">順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="090e6-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="090e6-116">_lpfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="090e6-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="090e6-117">順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="090e6-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="090e6-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="090e6-118">_ulFlags_</span></span>
  
> <span data-ttu-id="090e6-119">順番OLE **IStream**オブジェクトを通じてアクセスされるファイルの作成またはオープンを制御するために使用されるフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="090e6-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="090e6-120">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="090e6-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="090e6-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="090e6-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="090e6-122">**IStream**オブジェクトの一時ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="090e6-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="090e6-123">このフラグが設定されている場合は、STGM_CREATE と STGM_READWRITE のフラグも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="090e6-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="090e6-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="090e6-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="090e6-125">ファイルは、既に存在している場合でも作成されます。</span><span class="sxs-lookup"><span data-stu-id="090e6-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="090e6-126">_lpszfilename_パラメーターが設定されていない場合は、このフラグと STGM_DELETEONRELEASE の両方を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="090e6-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="090e6-127">STGM_CREATE が設定されている場合は、STGM_READWRITE フラグも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="090e6-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="090e6-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="090e6-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="090e6-129">**IStream**オブジェクトが解放されるときに、ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="090e6-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="090e6-130">_lpszfilename_パラメーターが設定されていない場合は、このフラグと STGM_CREATE の両方を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="090e6-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="090e6-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="090e6-131">STGM_READ</span></span> 
  
> <span data-ttu-id="090e6-132">ファイルを作成するか、読み取り専用アクセスで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="090e6-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="090e6-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="090e6-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="090e6-134">ファイルは読み取り/書き込みアクセス許可で作成または開くことができます。</span><span class="sxs-lookup"><span data-stu-id="090e6-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="090e6-135">このフラグが設定されていない場合は、STGM_CREATE フラグを設定しないでください。</span><span class="sxs-lookup"><span data-stu-id="090e6-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="090e6-136">_lpszfilename_</span><span class="sxs-lookup"><span data-stu-id="090e6-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="090e6-137">順番**openstreamonfile**が**IStream**オブジェクトを初期化するファイルのパスと拡張子を含む filename。</span><span class="sxs-lookup"><span data-stu-id="090e6-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="090e6-138">SOF_UNIQUEFILENAME フラグが設定されている場合、 _lpszfilename_には、一時ファイルを作成するディレクトリへのパスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="090e6-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="090e6-139">_lpszfilename_が NULL の場合、 **openstreamonfile**はシステムから適切なパスを取得し、STGM_CREATE と STGM_DELETEONRELEASE の両方のフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="090e6-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="090e6-140">_lpszprefix_</span><span class="sxs-lookup"><span data-stu-id="090e6-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="090e6-141">順番**openstreamonfile**が**IStream**オブジェクトを初期化するファイル名のプレフィックス。</span><span class="sxs-lookup"><span data-stu-id="090e6-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="090e6-142">設定されている場合、プレフィックスは3文字以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="090e6-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="090e6-143">_lpszprefix_が NULL の場合は、プレフィックス "SOF" が使用されます。</span><span class="sxs-lookup"><span data-stu-id="090e6-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="090e6-144">_lppstream_</span><span class="sxs-lookup"><span data-stu-id="090e6-144">_lppStream_</span></span>
  
> <span data-ttu-id="090e6-145">読み上げ**IStream**インターフェイスを公開しているオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="090e6-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="090e6-146">戻り値</span><span class="sxs-lookup"><span data-stu-id="090e6-146">Return value</span></span>

<span data-ttu-id="090e6-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="090e6-147">S_OK</span></span> 
  
> <span data-ttu-id="090e6-148">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="090e6-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="090e6-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="090e6-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="090e6-150">ユーザーのアクセス許可が不足しているため、または読み取り専用ファイルを変更できないため、ファイルにアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="090e6-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="090e6-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="090e6-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="090e6-152">指定したファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="090e6-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="090e6-153">解説</span><span class="sxs-lookup"><span data-stu-id="090e6-153">Remarks</span></span>

<span data-ttu-id="090e6-154">**openstreamonfile**関数には、SOF_UNIQUEFILENAME フラグの設定によって区別される、2つの重要な用途があります。</span><span class="sxs-lookup"><span data-stu-id="090e6-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="090e6-155">このフラグが設定されていない場合、 **openstreamonfile**は、istream オブジェクトを既存のファイルに開きます。たとえば、 \*\*\*\* istream を使用して添付ファイルの**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティにコンテンツをコピーします。 **:: CopyTo**メソッド。</span><span class="sxs-lookup"><span data-stu-id="090e6-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="090e6-156">この場合、 _lpszfilename_パラメーターには、ファイルのパスとファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="090e6-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="090e6-157">SOF_UNIQUEFILENAME が設定されている場合、 **openstreamonfile**は**IStream**オブジェクトのデータを保持するための一時ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="090e6-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="090e6-158">この使用法では、必要に応じて、ファイルを作成するディレクトリへのパスを_lpszfilename_パラメーターで指定できます。また、必要に応じて、 _lpszfilename_パラメーターでファイル名のプレフィックスを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="090e6-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="090e6-159">呼び出し元クライアントアプリケーションまたはサービスプロバイダーが**IStream**オブジェクトで終了すると、OLE **istream:: Release**メソッドを呼び出して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="090e6-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="090e6-160">MAPI では、特に、 _lpAllocateBuffer_および_lpfreebuffer_で参照されている関数を使用して、imapiprop などのオブジェクトインターフェイスを呼び出すときに、クライアントアプリケーションが使用するメモリを割り当て[ます。GetProps](imapiprop-getprops.md)と[IMAPITable:: QueryRows](imapitable-queryrows.md)。</span><span class="sxs-lookup"><span data-stu-id="090e6-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="090e6-161">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="090e6-161">Notes to callers</span></span>

<span data-ttu-id="090e6-162">SOF_UNIQUEFILENAME フラグは、メッセージングシステムに固有の名前を持つ一時ファイルを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="090e6-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="090e6-163">このフラグが設定されている場合、 _lpszfilename_パラメーターは一時ファイルのパスを指定し、 _lpszfilename_パラメーターにはファイル名の先頭文字が含まれます。</span><span class="sxs-lookup"><span data-stu-id="090e6-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="090e6-164">構築された<prefix>ファイル名は hhhhhhhh-hhhh-hhhh-hhhh-hhhhhhhhhhhh です。TMP、hhhhhhhh-hhhh-hhhh-hhhh-hhhhhhhhhhhh は16進数の数値です。</span><span class="sxs-lookup"><span data-stu-id="090e6-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="090e6-165">_lpszfilename_が NULL の場合は、Windows 関数**GetTempPath**から返される一時ファイルディレクトリ、または一時ファイルディレクトリが指定されていない場合は現在のディレクトリにファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="090e6-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="090e6-166">SOF_UNIQUEFILENAME フラグが設定されていない場合、 _lpszprefix_は無視され、 _lpszprefix_には開くまたは作成するファイルの完全修飾パスとファイル名が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="090e6-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="090e6-167">このファイルは、 _ulflags_に設定されている他のフラグに基づいて開かれるか作成されます。</span><span class="sxs-lookup"><span data-stu-id="090e6-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="090e6-168">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="090e6-168">MFCMAPI reference</span></span>

<span data-ttu-id="090e6-169">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="090e6-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="090e6-170">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="090e6-170">**File**</span></span>|<span data-ttu-id="090e6-171">**関数**</span><span class="sxs-lookup"><span data-stu-id="090e6-171">**Function**</span></span>|<span data-ttu-id="090e6-172">**コメント**</span><span class="sxs-lookup"><span data-stu-id="090e6-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="090e6-173">ファイル .cpp</span><span class="sxs-lookup"><span data-stu-id="090e6-173">File.cpp</span></span>  <br/> |<span data-ttu-id="090e6-174">writeattachstreamtofile</span><span class="sxs-lookup"><span data-stu-id="090e6-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="090e6-175">mfcmapi は、 **openstreamonfile**メソッドを使用してファイルのストリームを開き、添付ファイルに書き出すことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="090e6-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="090e6-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="090e6-176">See also</span></span>



<span data-ttu-id="090e6-177">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="090e6-177">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>


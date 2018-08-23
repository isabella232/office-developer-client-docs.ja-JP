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
ms.openlocfilehash: 8c246968dcac719a8ee8177e20e802f9c7033435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801701"
---
# <a name="openstreamonfile"></a><span data-ttu-id="dcc00-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="dcc00-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="dcc00-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dcc00-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dcc00-105">ファイルの内容にアクセスするのには OLE **IStream**オブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="dcc00-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="dcc00-106">この関数は、パスとファイルの拡張子、そのため、 [OpenStreamOnFileW](openstreamonfilew.md)では、この関数の Unicode バージョンの使用を含むファイル名が推奨されている ANSI 文字列を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="dcc00-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dcc00-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dcc00-107">Header file:</span></span>  <br/> |<span data-ttu-id="dcc00-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dcc00-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dcc00-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="dcc00-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="dcc00-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="dcc00-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="dcc00-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="dcc00-111">Called by:</span></span>  <br/> |<span data-ttu-id="dcc00-112">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="dcc00-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="dcc00-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dcc00-113">Parameters</span></span>

 <span data-ttu-id="dcc00-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="dcc00-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="dcc00-115">[in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dcc00-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="dcc00-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="dcc00-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="dcc00-117">[in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dcc00-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="dcc00-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dcc00-118">_ulFlags_</span></span>
  
> <span data-ttu-id="dcc00-119">[in]OLE **IStream**オブジェクトを通じてアクセスするのファイルを開くまたは作成を制御するために使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="dcc00-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="dcc00-120">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="dcc00-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="dcc00-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="dcc00-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="dcc00-122">一時ファイルは、 **IStream**オブジェクトを作成するのには。</span><span class="sxs-lookup"><span data-stu-id="dcc00-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="dcc00-123">このフラグが設定されている場合、STGM_CREATE と STGM_READWRITE のフラグも設定してください。</span><span class="sxs-lookup"><span data-stu-id="dcc00-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="dcc00-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="dcc00-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="dcc00-125">ファイルは、1 つ既に存在する場合でも作成すること。</span><span class="sxs-lookup"><span data-stu-id="dcc00-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="dcc00-126">_場合_パラメーターが設定されていない場合は、このフラグと STGM_DELETEONRELEASE の両方を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcc00-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="dcc00-127">STGM_CREATE が設定されている場合、STGM_READWRITE のフラグも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcc00-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="dcc00-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="dcc00-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="dcc00-129">ファイルでは、 **IStream**オブジェクトが解放されるときに削除されます。</span><span class="sxs-lookup"><span data-stu-id="dcc00-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="dcc00-130">_場合_パラメーターが設定されていない場合は、このフラグと STGM_CREATE の両方を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcc00-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="dcc00-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="dcc00-131">STGM_READ</span></span> 
  
> <span data-ttu-id="dcc00-132">ファイルは読み取り専用アクセスで開くまたは作成するのには。</span><span class="sxs-lookup"><span data-stu-id="dcc00-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="dcc00-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="dcc00-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="dcc00-134">ファイルは、読み取り/書き込み権限で開くまたは作成するのには。</span><span class="sxs-lookup"><span data-stu-id="dcc00-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="dcc00-135">このフラグが設定されていない場合、STGM_CREATE フラグする必要がありますを設定できませんか。</span><span class="sxs-lookup"><span data-stu-id="dcc00-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="dcc00-136">_場合_</span><span class="sxs-lookup"><span data-stu-id="dcc00-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="dcc00-137">[in]ファイル名、パスおよび**OpenStreamOnFile**が**IStream**オブジェクトを初期化する対象のファイルの拡張子を含みます。</span><span class="sxs-lookup"><span data-stu-id="dcc00-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="dcc00-138">SOF_UNIQUEFILENAME フラグが設定されている場合、_場合_に、一時ファイルを作成するためのディレクトリへのパスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="dcc00-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="dcc00-139">_場合_が NULL の場合は、 **OpenStreamOnFile**では、システムから適切なパスを取得し、STGM_CREATE と STGM_DELETEONRELEASE の両方のフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcc00-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="dcc00-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="dcc00-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="dcc00-141">[in]**OpenStreamOnFile**が**IStream**オブジェクトを初期化するファイル名の接頭辞。</span><span class="sxs-lookup"><span data-stu-id="dcc00-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="dcc00-142">かどうか設定すると、プレフィックスする必要がありますが含まれている以下の 3 文字です。</span><span class="sxs-lookup"><span data-stu-id="dcc00-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="dcc00-143">_LpszPrefix_が NULL の場合は、"SOF"の接頭辞を使用します。</span><span class="sxs-lookup"><span data-stu-id="dcc00-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="dcc00-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="dcc00-144">_lppStream_</span></span>
  
> <span data-ttu-id="dcc00-145">[out]**IStream**インターフェイスを公開するオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dcc00-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dcc00-146">�߂�l</span><span class="sxs-lookup"><span data-stu-id="dcc00-146">Return value</span></span>

<span data-ttu-id="dcc00-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="dcc00-147">S_OK</span></span> 
  
> <span data-ttu-id="dcc00-148">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="dcc00-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="dcc00-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="dcc00-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="dcc00-150">権限のないユーザーがファイルにアクセスできませんでしたか、読み取り専用ファイルを変更できないためです。</span><span class="sxs-lookup"><span data-stu-id="dcc00-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="dcc00-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dcc00-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="dcc00-152">指定のファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="dcc00-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dcc00-153">注釈</span><span class="sxs-lookup"><span data-stu-id="dcc00-153">Remarks</span></span>

<span data-ttu-id="dcc00-154">**OpenStreamOnFile**の関数には、SOF_UNIQUEFILENAME フラグの設定によって、2 つの重要な用途があります。</span><span class="sxs-lookup"><span data-stu-id="dcc00-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="dcc00-155">**OpenStreamOnFile**が**IStream**オブジェクトの例では、 **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) のプロパティに**IStream を使用して添付ファイルの内容をコピーするのには、既存のファイルを開きますこのフラグが設定されていない場合:: CopyTo**メソッドです。</span><span class="sxs-lookup"><span data-stu-id="dcc00-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="dcc00-156">ここで_場合_のパラメーターは、ファイルのファイル名とパスを指定します。</span><span class="sxs-lookup"><span data-stu-id="dcc00-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="dcc00-157">SOF_UNIQUEFILENAME を設定すると、 **OpenStreamOnFile**は、 **IStream**オブジェクトのデータを保持する一時ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="dcc00-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="dcc00-158">この使用方法の_場合_のパラメーターはオプションで、ファイルを作成するのには、 _lpszPrefix_パラメーターは、ファイル名のプレフィックスをオプションで指定できます、ディレクトリへのパスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="dcc00-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="dcc00-159">**IStream**オブジェクトには、呼び出し元のクライアント アプリケーションまたはサービス プロバイダーが終了したらは、OLE **IStream::Release**メソッドを呼び出すことによって解放にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcc00-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="dcc00-160">MAPI で示される_lpAllocateBuffer_および多くのメモリの割り当てと解放の_lpFreeBuffer_特に[IMAPIProp などのオブジェクトのインターフェイスを呼び出すときに、クライアント アプリケーションによって使用するメモリを割り当てることの機能を使用します。GetProps](imapiprop-getprops.md)と[IMAPITable::QueryRows](imapitable-queryrows.md)。</span><span class="sxs-lookup"><span data-stu-id="dcc00-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dcc00-161">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="dcc00-161">Notes to callers</span></span>

<span data-ttu-id="dcc00-162">メッセージング システムに固有の名前を持つ一時ファイルを作成するのには SOF_UNIQUEFILENAME フラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="dcc00-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="dcc00-163">このフラグが設定されている場合、一時ファイルと_lpszPrefix_パラメーターのパスである_場合_のパラメーターを指定には、ファイル名の先頭の文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dcc00-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="dcc00-164">構築されたファイル名は<prefix>HHHH。TMP は 16 進数です。</span><span class="sxs-lookup"><span data-stu-id="dcc00-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="dcc00-165">_場合_が NULL の場合は、ファイルは**値**では、Windows の機能から返される一時ファイルのディレクトリまたは現在のディレクトリに一時ファイルのディレクトリが指定されていない場合。</span><span class="sxs-lookup"><span data-stu-id="dcc00-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="dcc00-166">SOF_UNIQUEFILENAME フラグが設定されていない場合は、 _lpszPrefix_は無視され、_場合_は、開くまたは作成するファイルのファイル名と完全修飾パスを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcc00-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="dcc00-167">ファイルを開くか_ulFlags_に設定されている他のフラグを基に作成されます。</span><span class="sxs-lookup"><span data-stu-id="dcc00-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dcc00-168">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="dcc00-168">MFCMAPI reference</span></span>

<span data-ttu-id="dcc00-169">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="dcc00-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dcc00-170">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="dcc00-170">**File**</span></span>|<span data-ttu-id="dcc00-171">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="dcc00-171">**Function**</span></span>|<span data-ttu-id="dcc00-172">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="dcc00-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dcc00-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="dcc00-173">File.cpp</span></span>  <br/> |<span data-ttu-id="dcc00-174">WriteAttachStreamToFile</span><span class="sxs-lookup"><span data-stu-id="dcc00-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="dcc00-175">MFCMAPI では、 **OpenStreamOnFile**メソッドを使用して、添付ファイルがそれに書き出されますので、ファイル ストリームをオープンします。</span><span class="sxs-lookup"><span data-stu-id="dcc00-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dcc00-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="dcc00-176">See also</span></span>



<span data-ttu-id="dcc00-177">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="dcc00-177">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>


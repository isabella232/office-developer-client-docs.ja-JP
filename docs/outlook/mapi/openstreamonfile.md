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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439094"
---
# <a name="openstreamonfile"></a><span data-ttu-id="1b5a0-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="1b5a0-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="1b5a0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b5a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b5a0-105">ファイルの内容にアクセスするために OLE **IStream** オブジェクトを割り当て、初期化します。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="1b5a0-106">この関数は、パスとファイル拡張子を含むファイル名として ANSI 文字列を受け取ります。したがって、この関数の Unicode バージョン [である OpenStreamOnFileW](openstreamonfilew.md)の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b5a0-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1b5a0-107">Header file:</span></span>  <br/> |<span data-ttu-id="1b5a0-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1b5a0-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1b5a0-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="1b5a0-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="1b5a0-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="1b5a0-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="1b5a0-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="1b5a0-111">Called by:</span></span>  <br/> |<span data-ttu-id="1b5a0-112">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1b5a0-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="1b5a0-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1b5a0-113">Parameters</span></span>

 <span data-ttu-id="1b5a0-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="1b5a0-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="1b5a0-115">[in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="1b5a0-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="1b5a0-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="1b5a0-117">[in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="1b5a0-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b5a0-118">_ulFlags_</span></span>
  
> <span data-ttu-id="1b5a0-119">[in]OLE IStream オブジェクトを介してアクセスするファイルの作成または開きを制御するために使用されるフラグ **のビット** マスク。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="1b5a0-120">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="1b5a0-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="1b5a0-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="1b5a0-122">IStream オブジェクト用に一時ファイル **を作成する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="1b5a0-123">このフラグが設定されている場合は、STGM_CREATEおよびSTGM_READWRITEフラグも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="1b5a0-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="1b5a0-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="1b5a0-125">ファイルは、既に存在している場合でも作成されます。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="1b5a0-126">_lpszFileName_ パラメーターが設定されていない場合は、このフラグとSTGM_DELETEONRELEASE設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="1b5a0-127">このSTGM_CREATE設定されている場合は、STGM_READWRITEフラグも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="1b5a0-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="1b5a0-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="1b5a0-129">**IStream** オブジェクトが解放されると、ファイルは削除されます。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="1b5a0-130">_lpszFileName_ パラメーターが設定されていない場合は、このフラグとSTGM_CREATE設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="1b5a0-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="1b5a0-131">STGM_READ</span></span> 
  
> <span data-ttu-id="1b5a0-132">ファイルは、読み取り専用アクセスで作成または開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="1b5a0-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="1b5a0-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="1b5a0-134">ファイルを作成するか、読み取り/書き込み権限で開きます。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="1b5a0-135">このフラグが設定されていない場合、STGM_CREATEフラグも設定できません。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="1b5a0-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="1b5a0-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="1b5a0-137">[in] **OpenStreamOnFile** が **IStream** オブジェクトを初期化するファイルのファイル名 (パスと拡張子を含む)。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="1b5a0-138">SOF_UNIQUEFILENAMEフラグが設定されている場合  _、lpszFileName_ には、一時ファイルを作成するディレクトリへのパスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="1b5a0-139">_lpszFileName_ が NULL の場合 **、OpenStreamOnFile** はシステムから適切なパスを取得し、STGM_CREATE フラグと STGM_DELETEONRELEASE フラグの両方を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="1b5a0-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="1b5a0-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="1b5a0-141">[in] **OpenStreamOnFile** が IStream オブジェクトを初期化するファイル名 **のプレフィックス** 。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="1b5a0-142">設定する場合、プレフィックスには 3 文字以内で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="1b5a0-143">_lpszPrefix が_ NULL の場合は、"SOF" のプレフィックスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="1b5a0-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="1b5a0-144">_lppStream_</span></span>
  
> <span data-ttu-id="1b5a0-145">[out] **IStream** インターフェイスを公開するオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1b5a0-146">戻り値</span><span class="sxs-lookup"><span data-stu-id="1b5a0-146">Return value</span></span>

<span data-ttu-id="1b5a0-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b5a0-147">S_OK</span></span> 
  
> <span data-ttu-id="1b5a0-148">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="1b5a0-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="1b5a0-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1b5a0-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="1b5a0-150">ユーザーのアクセス許可が不足しているか、読み取り専用ファイルを変更できないため、ファイルにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="1b5a0-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1b5a0-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1b5a0-152">指定されたファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b5a0-153">注釈</span><span class="sxs-lookup"><span data-stu-id="1b5a0-153">Remarks</span></span>

<span data-ttu-id="1b5a0-154">**OpenStreamOnFile** 関数には、2 つの重要な用途があります。このフラグの設定SOF_UNIQUEFILENAMEします。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="1b5a0-155">このフラグを設定しない場合 **、OpenStreamOnFile** は既存のファイルで **IStream** オブジェクトを開きます。たとえば、その内容を **IStream::CopyTo** メソッドを使用して添付ファイルの **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="1b5a0-156">この場合  _、lpszFileName_ パラメーターは、ファイルのパスとファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="1b5a0-157">このSOF_UNIQUEFILENAME **設定すると、OpenStreamOnFile** は IStream オブジェクトのデータを保持する一時ファイル **を作成** します。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="1b5a0-158">この使用法では  _、lpszFileName_ パラメーターは、必要に応じて、ファイルを作成するディレクトリへのパスを指定し  _、lpszPrefix_ パラメーターはオプションでファイル名のプレフィックスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="1b5a0-159">呼び出し元のクライアント アプリケーションまたはサービス プロバイダーが **IStream** オブジェクトで終了したら、OLE **IStream::Release** メソッドを呼び出して解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="1b5a0-160">MAPI は、ほとんどのメモリ割り当ておよび割り当て解除に  _lpAllocateBuffer_ と  _lpFreeBuffer_ が指す関数を使用します。特に [、IMAPIProp::GetProps](imapiprop-getprops.md) や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際に、クライアント アプリケーションで使用するメモリを割り当てる場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b5a0-161">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1b5a0-161">Notes to callers</span></span>

<span data-ttu-id="1b5a0-162">メッセージ SOF_UNIQUEFILENAMEフラグを使用して、メッセージング システム固有の名前を持つ一時ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="1b5a0-163">このフラグを設定すると  _、lpszFileName_ パラメーターは一時ファイルのパスを指定し  _、lpszPrefix_ パラメーターにはファイル名のプレフィックス文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="1b5a0-164">構築されたファイル名は <prefix> HHHH です。TMP。HHHH は 16 進数です。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="1b5a0-165">_lpszFileName_ が NULL の場合、ファイルは Windows 関数 **GetTempPath** から返される一時ファイル ディレクトリ、または一時ファイル ディレクトリが指定されていない場合はカレント ディレクトリに作成されます。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="1b5a0-166">SOF_UNIQUEFILENAME フラグが設定されていない場合  _、lpszPrefix_ は無視され  _、lpszFileName_ には、開くまたは作成するファイルの完全修飾パスとファイル名を含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="1b5a0-167">ファイルは  _、ulFlags_ で設定されている他のフラグに基づいて開かまたは作成されます。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1b5a0-168">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="1b5a0-168">MFCMAPI reference</span></span>

<span data-ttu-id="1b5a0-169">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1b5a0-170">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="1b5a0-170">**File**</span></span>|<span data-ttu-id="1b5a0-171">**関数**</span><span class="sxs-lookup"><span data-stu-id="1b5a0-171">**Function**</span></span>|<span data-ttu-id="1b5a0-172">**コメント**</span><span class="sxs-lookup"><span data-stu-id="1b5a0-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1b5a0-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="1b5a0-173">File.cpp</span></span>  <br/> |<span data-ttu-id="1b5a0-174">WriteAttachStreamToFile</span><span class="sxs-lookup"><span data-stu-id="1b5a0-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="1b5a0-175">MFCMAPI では **、OpenStreamOnFile** メソッドを使用してファイル上のストリームを開き、添付ファイルを書き出します。</span><span class="sxs-lookup"><span data-stu-id="1b5a0-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b5a0-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b5a0-176">See also</span></span>



<span data-ttu-id="1b5a0-177">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1b5a0-177">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>


---
title: ニックネーム キャッシュ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: '最終更新日: 2013 年1月30日'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334518"
---
# <a name="nickname-cache"></a><span data-ttu-id="7440b-103">ニックネーム キャッシュ</span><span class="sxs-lookup"><span data-stu-id="7440b-103">Nickname cache</span></span>

 
  
<span data-ttu-id="7440b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7440b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7440b-105">microsoft Office Outlook 2007、microsoft outlook 2010、および microsoft outlook 2013 は、"オートコンプリートストリーム" とも呼ばれるニックネームキャッシュを操作します。</span><span class="sxs-lookup"><span data-stu-id="7440b-105">Microsoft Office Outlook 2007, Microsoft Outlook 2010, and Microsoft Outlook 2013 interact with the nickname cache, also known as the "autocomplete stream."</span></span> <span data-ttu-id="7440b-106">オートコンプリートストリームは、Outlook では、ユーザーが電子メールを作成している間に [**宛先**]、[ **Cc**]、および [ **Bcc** ] の各編集ボックスに表示される名前の一覧を保持します。</span><span class="sxs-lookup"><span data-stu-id="7440b-106">The autocomplete stream is where Outlook persists the autocomplete list, which is the list of names that displays in the **To**, **Cc**, and **Bcc** edit boxes while a user is composing an email.</span></span> <span data-ttu-id="7440b-107">このトピックでは、outlook 2007、outlook 2010、および outlook 2013 がオートコンプリートストリームを操作する方法について説明し、ファイルのバイナリ形式およびオートコンプリートストリームと対話するための推奨される方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="7440b-107">This topic describes how Outlook 2007, Outlook 2010, and Outlook 2013 interact with the autocomplete stream and also discusses the binary format of the file and the recommended ways for interacting with the autocomplete stream.</span></span> 
  
<span data-ttu-id="7440b-108">outlook 2010 または outlook 2013 と対話するアプリケーションでは、オートコンプリートストリームは mapi プロパティとして格納され、メッセージの mapi または**PropertyAccessor**オブジェクトを使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="7440b-108">For applications that interact with Outlook 2010 or Outlook 2013, the autocomplete stream is stored as a MAPI property and can be modified using the MAPI or the **PropertyAccessor** object of the message.</span></span> <span data-ttu-id="7440b-109">**PropertyAccessor**オブジェクトは、outlook 2010 または outlook 2013 オブジェクトモデルで公開されます。</span><span class="sxs-lookup"><span data-stu-id="7440b-109">The **PropertyAccessor** object is exposed in the Outlook 2010 or Outlook 2013 object models.</span></span> 
  
<span data-ttu-id="7440b-110">Outlook 2007 オブジェクトモデルまたは MAPI api に依存関係はありません。</span><span class="sxs-lookup"><span data-stu-id="7440b-110">There are no dependencies on the Outlook 2007 object model or MAPI APIs.</span></span> <span data-ttu-id="7440b-111">そのため、Outlook 2007 内のオートコンプリートストリームに変更を加えるアプリケーションは、任意のプログラミング言語を使用して記述できます。</span><span class="sxs-lookup"><span data-stu-id="7440b-111">Therefore, applications that make changes to the autocomplete stream within Outlook 2007 can be written using any programming language.</span></span>
  
## <a name="interacting-with-the-autocomplete-stream"></a><span data-ttu-id="7440b-112">オートコンプリートストリームとの対話</span><span class="sxs-lookup"><span data-stu-id="7440b-112">Interacting with the Autocomplete Stream</span></span>

<span data-ttu-id="7440b-113">[**宛先**]、[ **Cc**]、または [ **Bcc** ] 編集ボックスにメッセージがアクセスされると、オートコンプリートストリームが読み込まれ、ユーザー名の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7440b-113">When the **To**, **Cc**, or **Bcc** edit boxes are accessed on a message, the autocomplete stream is loaded and the list of user names is displayed.</span></span> <span data-ttu-id="7440b-114">Outlook は、次の2つの方法で、オートコンプリートストリームと対話します。</span><span class="sxs-lookup"><span data-stu-id="7440b-114">Outlook interacts with the autocomplete stream in two ways:</span></span> 
  
1. <span data-ttu-id="7440b-115">オートコンプリートストリームを読み込む</span><span class="sxs-lookup"><span data-stu-id="7440b-115">Loading the autocomplete stream</span></span> 
    
2. <span data-ttu-id="7440b-116">オートコンプリートストリームのデータに加えた変更を保存する</span><span class="sxs-lookup"><span data-stu-id="7440b-116">Saving changes to the data in the autocomplete stream</span></span>
    
<span data-ttu-id="7440b-117">次に示すように、オートコンプリートデータを保存する方法は、outlook 2007 と outlook 2010 または outlook 2013 で異なります。</span><span class="sxs-lookup"><span data-stu-id="7440b-117">The means of storing the autocomplete data differs between Outlook 2007 and Outlook 2010 or Outlook 2013 as follows:</span></span> 
  
 <span data-ttu-id="7440b-118">**Outlook 2007**</span><span class="sxs-lookup"><span data-stu-id="7440b-118">**Outlook 2007**</span></span>
  
<span data-ttu-id="7440b-119">Outlook 2007 では、オートコンプリートストリームはプロファイルと同じ名前のファイルに格納され、拡張子は nk2 になります。</span><span class="sxs-lookup"><span data-stu-id="7440b-119">For Outlook 2007, the autocomplete stream is stored in a file with the same name as the profile and an extension of .nk2.</span></span> <span data-ttu-id="7440b-120">たとえば、既定の "outlook" プロファイルが使用されている場合、ファイルは "nk2" という名前になります。</span><span class="sxs-lookup"><span data-stu-id="7440b-120">For example, if the default profile of "outlook" is used, the file will be called "outlook.nk2".</span></span> <span data-ttu-id="7440b-121">nk2 ファイルは%APPDATA%\Microsoft\Outlook. に保存されます。</span><span class="sxs-lookup"><span data-stu-id="7440b-121">The .nk2 file is stored in %APPDATA%\Microsoft\Outlook.</span></span> <span data-ttu-id="7440b-122">ニックネームキャッシュバイナリファイル形式の詳細については、「 [Outlook 2003/2007 NK2 ファイル形式と開発者ガイドライン](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7440b-122">For more information about the nickname cache binary file format, see [Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).</span></span>
  
 <span data-ttu-id="7440b-123">**outlook 2010 および outlook 2013**</span><span class="sxs-lookup"><span data-stu-id="7440b-123">**Outlook 2010 and Outlook 2013**</span></span>
  
<span data-ttu-id="7440b-124">outlook 2010 または outlook 2013 は、メールアカウントの配信ストアの受信トレイにある [関連付けられたコンテンツ] テーブル内のメッセージから、オートコンプリートストリームを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="7440b-124">Outlook 2010 or Outlook 2013 reads the autocomplete stream from a message in the Associated Contents table of the Inbox of the mail account's delivery store.</span></span> <span data-ttu-id="7440b-125">この隠しメッセージには、メッセージクラスと IPM の件名があります。構成のオートコンプリート。</span><span class="sxs-lookup"><span data-stu-id="7440b-125">This hidden message has a message class and subject of IPM.Configuration.Autocomplete.</span></span> <span data-ttu-id="7440b-126">オートコンプリートストリームは、このメッセージの PR_ROAMING_BINARYSTREAM プロパティ ([PidTagRoamingBinary 標準プロパティ](pidtagroamingbinary-canonical-property.md)) に格納されます。</span><span class="sxs-lookup"><span data-stu-id="7440b-126">The autocomplete stream is stored on this message in the PR_ROAMING_BINARYSTREAM property ([PidTagRoamingBinary Canonical Property](pidtagroamingbinary-canonical-property.md)).</span></span> <span data-ttu-id="7440b-127">オートコンプリートデータが%USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. にある自動保存ファイルに一時的にキャッシュされることがあります。</span><span class="sxs-lookup"><span data-stu-id="7440b-127">The autocomplete data may be temporarily cached in an autocomplete .dat file located in %USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache.</span></span> <span data-ttu-id="7440b-128">ただし、.dat ファイルはキャッシュのみであり、ユーザーが outlook 2010 または outlook 2013 を終了するときに配信ストアに書き戻すためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="7440b-128">However, the .dat file is only a cache and is not used to write back to the delivery store when the user exits Outlook 2010 or Outlook 2013.</span></span>
  
## <a name="loading-the-autocomplete-stream"></a><span data-ttu-id="7440b-129">オートコンプリートストリームを読み込む</span><span class="sxs-lookup"><span data-stu-id="7440b-129">Loading the Autocomplete Stream</span></span>

<span data-ttu-id="7440b-130">Outlook は、アドレス指定機能を持つアイテムが初期化されるたびに、オートコンプリートストリームを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="7440b-130">Outlook loads the autocomplete stream whenever an item with addressing functionality is initialized.</span></span> <span data-ttu-id="7440b-131">たとえば、新しいメール、メールの返信、連絡先アイテム、会議出席依頼などの電子メールアドレスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7440b-131">For example, email addresses are used in a new mail, a mail reply, a contact item, a meeting request, and so on.</span></span> <span data-ttu-id="7440b-132">データを読み込むために、Outlook はストリームのすべての内容をメモリに読み取ります。</span><span class="sxs-lookup"><span data-stu-id="7440b-132">To load the data, Outlook reads all of the contents of the stream into memory.</span></span>
  
<span data-ttu-id="7440b-133">オートコンプリート操作の場合、outlook は、outlook .exe プロセスの有効期間中は、このようなインメモリ構造に排他的に作用します。</span><span class="sxs-lookup"><span data-stu-id="7440b-133">For autocomplete operations, Outlook interacts exclusively with this in-memory structure for the duration of the outlook.exe process lifetime.</span></span> <span data-ttu-id="7440b-134">Outlook では、この構造体はシャットダウン時にのみ保存されます。</span><span class="sxs-lookup"><span data-stu-id="7440b-134">Outlook only saves the structure on shutdown.</span></span> <span data-ttu-id="7440b-135">このプロセスの詳細については、次のセクション「オートコンプリートストリームの保存」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7440b-135">See the following section "Saving the Autocomplete Stream" for more information on this process.</span></span>
  
## <a name="saving-the-autocomplete-stream"></a><span data-ttu-id="7440b-136">オートコンプリートストリームの保存</span><span class="sxs-lookup"><span data-stu-id="7440b-136">Saving the Autocomplete Stream</span></span>

<span data-ttu-id="7440b-137">次のいずれかの方法でオートコンプリートの一覧が変更された場合、Outlook は、オートコンプリートストリームをシャットダウン時に保存します。</span><span class="sxs-lookup"><span data-stu-id="7440b-137">Outlook saves the autocomplete stream on shutdown if the autocomplete list has changed in any of the following ways:</span></span>
  
- <span data-ttu-id="7440b-138">名前の解決、[アドレス帳] ダイアログからの受信者の選択、またはまだリストにない受信者へのメールの送信によって、新しいニックネームエントリが追加されます。</span><span class="sxs-lookup"><span data-stu-id="7440b-138">A new nickname entry is added through resolving a name, picking a recipient from the address book dialog, or sending mail to a recipient that was not already in the list.</span></span>
    
- <span data-ttu-id="7440b-139">エントリは、リスト内の既存の受信者にメールを送信することによって変更されます。</span><span class="sxs-lookup"><span data-stu-id="7440b-139">An entry is modified by sending mail to an existing recipient in the list.</span></span>
    
- <span data-ttu-id="7440b-140">ユーザーが UI を通じてエントリを削除します。</span><span class="sxs-lookup"><span data-stu-id="7440b-140">An entry is removed by the user through the UI.</span></span>
    
- <span data-ttu-id="7440b-141">その他の重要なシナリオは、このトピックに関連していません。</span><span class="sxs-lookup"><span data-stu-id="7440b-141">Other minor scenarios not relevant to this topic.</span></span>
    
<span data-ttu-id="7440b-142">オートコンプリートデータへの変更を保存するには、メモリ内構造を[オートコンプリートストリーム](autocomplete-stream.md)に書き戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7440b-142">Saving changes to the autocomplete data involves writing the in-memory structure back to an [Autocomplete Stream](autocomplete-stream.md).</span></span> <span data-ttu-id="7440b-143">Outlook 2007 と対話する場合、stream はローカルの nk2 ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="7440b-143">When interacting with Outlook 2007, the stream is saved to a local .nk2 file.</span></span> <span data-ttu-id="7440b-144">outlook 2010 または outlook 2013 の場合、オートコンプリートストリームは、メールアカウントの配信ストアの受信トレイの関連コンテンツテーブルに書き戻します。</span><span class="sxs-lookup"><span data-stu-id="7440b-144">For Outlook 2010 or Outlook 2013, the autocomplete stream writes back to the Associated Contents table of the Inbox of the mail account's delivery store.</span></span>
  
## <a name="recommendations"></a><span data-ttu-id="7440b-145">推奨事項</span><span class="sxs-lookup"><span data-stu-id="7440b-145">Recommendations</span></span>

- <span data-ttu-id="7440b-146">オートコンプリートストリームを部分的に変更することはありません。</span><span class="sxs-lookup"><span data-stu-id="7440b-146">Never partially modify the autocomplete stream.</span></span> <span data-ttu-id="7440b-147">サポートされている相互作用は、すべてのオートコンプリートストリームをメモリに読み取り、2) メモリ構造を変更し、3) メールアカウントの配信ストアの受信トレイの関連するコンテンツテーブルにストリーム全体を書き込む (Outlook 2010 またはoutlook 2013) または nk2 ファイル (outlook 2007)。</span><span class="sxs-lookup"><span data-stu-id="7440b-147">The supported interaction is to 1) read the entire autocomplete stream into memory, 2) modify the memory structure, and 3) write the entire stream back to either the Associated Contents table of the Inbox of the mail account's delivery store (for Outlook 2010 or Outlook 2013) or to the local .nk2 file (Outlook 2007).</span></span>
    
- <span data-ttu-id="7440b-148">Outlook の実行中は、オートコンプリートストリームと対話しません。</span><span class="sxs-lookup"><span data-stu-id="7440b-148">Do not interact with the autocomplete stream while Outlook is running.</span></span> <span data-ttu-id="7440b-149">ストリームを変更している間に Outlook が実行されている場合は、シャットダウン時に変更内容が上書きされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7440b-149">If Outlook is running while you modify the stream, it will likely overwrite your changes when it shuts down.</span></span>
    
- <span data-ttu-id="7440b-150">PT_MV_UNICODE および PR_MV_STRING8 型のプロパティを、Microsoft Outlook 2003 で使用されるオートコンプリートストリームに書き込むことはできません。</span><span class="sxs-lookup"><span data-stu-id="7440b-150">Do not write properties of type PT_MV_UNICODE and PR_MV_STRING8 into an autocomplete stream to be consumed by Microsoft Outlook 2003.</span></span> <span data-ttu-id="7440b-151">これらのプロパティは、outlook 2007、outlook 2010、および outlook 2013 でのみ認識されます。</span><span class="sxs-lookup"><span data-stu-id="7440b-151">These properties are only understood by Outlook 2007, Outlook 2010, and Outlook 2013.</span></span>
    
- <span data-ttu-id="7440b-152">Outlook 2007 と対話するコードを開発する場合は、他のプロセスによって、nk2 ファイルを変更しないようにすることをお勧めします。これは、標準的\*\*\*\* なファイルロック api (たとえば、C/c + +**で LockFile) を使用して読み取りおよび書き込みを行っています。** C# でのロック)。</span><span class="sxs-lookup"><span data-stu-id="7440b-152">When developing code that interacts with Outlook 2007, we recommend that you lock the .nk2 file from modification by other processes while you are reading and writing it using standard file locking APIs (for example, **LockFile** in C/C++ and **FileStream.Lock** in C#).</span></span> 
    
- <span data-ttu-id="7440b-153">オートコンプリートストリームの行セットにある型のプロパティのみを変更します。</span><span class="sxs-lookup"><span data-stu-id="7440b-153">Only modify the properties of types that are from the row-set of the autocomplete stream.</span></span> <span data-ttu-id="7440b-154">オートコンプリートストリームのプロパティとプロパティの種類の詳細については、「 [autocomplete stream](autocomplete-stream.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7440b-154">For more information about the autocomplete stream properties and property types, see [Autocomplete Stream](autocomplete-stream.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7440b-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="7440b-155">See also</span></span>



[<span data-ttu-id="7440b-156">オートコンプリートストリーム</span><span class="sxs-lookup"><span data-stu-id="7440b-156">Autocomplete Stream</span></span>](autocomplete-stream.md)
  
[<span data-ttu-id="7440b-157">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="7440b-157">MAPI Profiles</span></span>](mapi-profiles.md)


[<span data-ttu-id="7440b-158">Outlook 2003/2007 NK2 ファイル形式と開発者ガイドライン</span><span class="sxs-lookup"><span data-stu-id="7440b-158">Outlook 2003/2007 NK2 File Format and Developer Guidelines</span></span>](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)


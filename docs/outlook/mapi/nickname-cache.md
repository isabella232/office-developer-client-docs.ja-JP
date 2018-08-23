---
title: ニックネーム キャッシュ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: '最終更新日: 2013 年 1 月 30 日'
ms.openlocfilehash: 547733f815c7d8c8762e79febce40ee9fec07d3a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574532"
---
# <a name="nickname-cache"></a><span data-ttu-id="4d5cf-103">ニックネーム キャッシュ</span><span class="sxs-lookup"><span data-stu-id="4d5cf-103">Nickname cache</span></span>

 
  
<span data-ttu-id="4d5cf-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d5cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d5cf-105">Microsoft Office Outlook 2007、Microsoft Outlook 2010 では、および Microsoft Outlook 2013 の対話、ニックネームのキャッシュとも呼ばれる「オートコンプリートのストリーム。」</span><span class="sxs-lookup"><span data-stu-id="4d5cf-105">Microsoft Office Outlook 2007, Microsoft Outlook 2010, and Microsoft Outlook 2013 interact with the nickname cache, also known as the "autocomplete stream."</span></span> <span data-ttu-id="4d5cf-106">オートコンプリートのストリームでは、Outlook には、オートコンプリートの一覧**に** **[cc]**、[表示名のリストが引き続き発生して、ユーザーが電子メールを作成するときに、 **[Bcc** ] ボックス。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-106">The autocomplete stream is where Outlook persists the autocomplete list, which is the list of names that displays in the **To**, **Cc**, and **Bcc** edit boxes while a user is composing an email.</span></span> <span data-ttu-id="4d5cf-107">このトピックでは、Outlook 2007 と Outlook 2010、Outlook 2013 がオートコンプリートのストリームとどのようにやり取りする方法について説明し、オートコンプリートのストリームと対話するための推奨される方法と、ファイルのバイナリ形式についても説明します。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-107">This topic describes how Outlook 2007, Outlook 2010, and Outlook 2013 interact with the autocomplete stream and also discusses the binary format of the file and the recommended ways for interacting with the autocomplete stream.</span></span> 
  
<span data-ttu-id="4d5cf-108">Outlook 2010 または Outlook 2013 とやり取りするアプリケーションの場合は、オートコンプリートのストリームが MAPI プロパティとして格納されているし、MAPI またはメッセージの**PropertyAccessor**オブジェクトを使用して変更することができます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-108">For applications that interact with Outlook 2010 or Outlook 2013, the autocomplete stream is stored as a MAPI property and can be modified using the MAPI or the **PropertyAccessor** object of the message.</span></span> <span data-ttu-id="4d5cf-109">**PropertyAccessor**オブジェクトは、Outlook 2010 または Outlook 2013 オブジェクト モデルで公開されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-109">The **PropertyAccessor** object is exposed in the Outlook 2010 or Outlook 2013 object models.</span></span> 
  
<span data-ttu-id="4d5cf-110">Outlook 2007 オブジェクト モデルまたは MAPI Api への依存関係はありません。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-110">There are no dependencies on the Outlook 2007 object model or MAPI APIs.</span></span> <span data-ttu-id="4d5cf-111">したがって、Outlook 2007 のオートコンプリートのストリームを変更するアプリケーションは、任意のプログラミング言語を使用して記述できます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-111">Therefore, applications that make changes to the autocomplete stream within Outlook 2007 can be written using any programming language.</span></span>
  
## <a name="interacting-with-the-autocomplete-stream"></a><span data-ttu-id="4d5cf-112">オートコンプリートのストリームを操作します。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-112">Interacting with the Autocomplete Stream</span></span>

<span data-ttu-id="4d5cf-113">メッセージでアクセスすると、**宛先**、 **Cc**、または [ **Bcc**のエディット ボックスのように、オートコンプリートのストリームが読み込まれ、ユーザー名の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-113">When the **To**, **Cc**, or **Bcc** edit boxes are accessed on a message, the autocomplete stream is loaded and the list of user names is displayed.</span></span> <span data-ttu-id="4d5cf-114">Outlook は、2 つの方法でオートコンプリート ストリームと対話します。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-114">Outlook interacts with the autocomplete stream in two ways:</span></span> 
  
1. <span data-ttu-id="4d5cf-115">オートコンプリートのストリームの読み込み</span><span class="sxs-lookup"><span data-stu-id="4d5cf-115">Loading the autocomplete stream</span></span> 
    
2. <span data-ttu-id="4d5cf-116">オートコンプリートのストリーム内のデータに変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-116">Saving changes to the data in the autocomplete stream</span></span>
    
<span data-ttu-id="4d5cf-117">オートコンプリートのデータを格納するための手段は、次のように Outlook 2007 および Outlook 2010 または Outlook 2013 の間で異なります。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-117">The means of storing the autocomplete data differs between Outlook 2007 and Outlook 2010 or Outlook 2013 as follows:</span></span> 
  
 <span data-ttu-id="4d5cf-118">**Outlook 2007**</span><span class="sxs-lookup"><span data-stu-id="4d5cf-118">**Outlook 2007**</span></span>
  
<span data-ttu-id="4d5cf-119">Outlook 2007 では、オートコンプリートのストリームは、同じ名前のプロファイルと .nk2 という拡張子を持つファイルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-119">For Outlook 2007, the autocomplete stream is stored in a file with the same name as the profile and an extension of .nk2.</span></span> <span data-ttu-id="4d5cf-120">たとえば、"outlook"の既定のプロファイルを使用する場合、"outlook.nk2"にファイルが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-120">For example, if the default profile of "outlook" is used, the file will be called "outlook.nk2".</span></span> <span data-ttu-id="4d5cf-121">.Nk2 ファイルは、%appdata%\microsoft\outlook に格納されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-121">The .nk2 file is stored in %APPDATA%\Microsoft\Outlook.</span></span> <span data-ttu-id="4d5cf-122">ニックネーム キャッシュのバイナリ ファイル形式の詳細については、 [Outlook 2003/2007 NK2 ファイル形式と開発者のガイドライン](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-122">For more information about the nickname cache binary file format, see [Outlook 2003/2007 NK2 File Format and Developer Guidelines](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).</span></span>
  
 <span data-ttu-id="4d5cf-123">**Outlook 2010、Outlook 2013**</span><span class="sxs-lookup"><span data-stu-id="4d5cf-123">**Outlook 2010 and Outlook 2013**</span></span>
  
<span data-ttu-id="4d5cf-124">Outlook 2010 または Outlook 2013 は、メール アカウントの配信ストアの受信トレイの内容を関連付けられているテーブル内のメッセージからオートコンプリートのストリームを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-124">Outlook 2010 or Outlook 2013 reads the autocomplete stream from a message in the Associated Contents table of the Inbox of the mail account's delivery store.</span></span> <span data-ttu-id="4d5cf-125">この隠しメッセージがあり、メッセージ クラス IPM の件名です。Configuration.Autocomplete。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-125">This hidden message has a message class and subject of IPM.Configuration.Autocomplete.</span></span> <span data-ttu-id="4d5cf-126">オートコンプリートのストリームは、PR_ROAMING_BINARYSTREAM プロパティ ([PidTagRoamingBinary の標準的なプロパティ](pidtagroamingbinary-canonical-property.md)) では、このメッセージに格納されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-126">The autocomplete stream is stored on this message in the PR_ROAMING_BINARYSTREAM property ([PidTagRoamingBinary Canonical Property](pidtagroamingbinary-canonical-property.md)).</span></span> <span data-ttu-id="4d5cf-127">%Userprofile%\appdata\local\microsoft\outlook\roamcache 内にある、オートコンプリートの .dat ファイルで、オートコンプリートのデータを一時的にキャッシュ可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-127">The autocomplete data may be temporarily cached in an autocomplete .dat file located in %USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache.</span></span> <span data-ttu-id="4d5cf-128">ただし、.dat ファイルはキャッシュのみであり、Outlook 2010 または Outlook 2013 を終了するとき、配信ストアへの書き戻しには使われません。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-128">However, the .dat file is only a cache and is not used to write back to the delivery store when the user exits Outlook 2010 or Outlook 2013.</span></span>
  
## <a name="loading-the-autocomplete-stream"></a><span data-ttu-id="4d5cf-129">オートコンプリートのストリームの読み込み</span><span class="sxs-lookup"><span data-stu-id="4d5cf-129">Loading the Autocomplete Stream</span></span>

<span data-ttu-id="4d5cf-130">Outlook は、アドレス指定機能を持つ項目が初期化されるたびに、オートコンプリートのストリームを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-130">Outlook loads the autocomplete stream whenever an item with addressing functionality is initialized.</span></span> <span data-ttu-id="4d5cf-131">たとえば、電子メール アドレスは、新着メール、メールの返信、連絡先アイテム、会議出席依頼、およびなどで使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-131">For example, email addresses are used in a new mail, a mail reply, a contact item, a meeting request, and so on.</span></span> <span data-ttu-id="4d5cf-132">データを読み込むには、Outlook は、すべてのストリームの内容をメモリに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-132">To load the data, Outlook reads all of the contents of the stream into memory.</span></span>
  
<span data-ttu-id="4d5cf-133">オートコンプリート機能の操作を Outlook はこのメモリ内の構造体だけを outlook.exe プロセスの有効期間の間に対話します。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-133">For autocomplete operations, Outlook interacts exclusively with this in-memory structure for the duration of the outlook.exe process lifetime.</span></span> <span data-ttu-id="4d5cf-134">Outlook はシャット ダウン時にのみ、構造を保存します。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-134">Outlook only saves the structure on shutdown.</span></span> <span data-ttu-id="4d5cf-135">このプロセスの詳細については、次のセクション「[オートコンプリート ストリームを保存」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-135">See the following section "Saving the Autocomplete Stream" for more information on this process.</span></span>
  
## <a name="saving-the-autocomplete-stream"></a><span data-ttu-id="4d5cf-136">オートコンプリートのストリームを保存します。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-136">Saving the Autocomplete Stream</span></span>

<span data-ttu-id="4d5cf-137">オートコンプリート リストは、次の方法のいずれかで変更された場合、outlook はシャット ダウン時にオートコンプリートのストリームを保存します。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-137">Outlook saves the autocomplete stream on shutdown if the autocomplete list has changed in any of the following ways:</span></span>
  
- <span data-ttu-id="4d5cf-138">名前を解決する、アドレス帳ダイアログ ボックスで、受信者を選択、またはまだリストされていない受信者にメールを送信することによって、新しいニックネーム エントリが追加されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-138">A new nickname entry is added through resolving a name, picking a recipient from the address book dialog, or sending mail to a recipient that was not already in the list.</span></span>
    
- <span data-ttu-id="4d5cf-139">エントリを変更するには、リスト内の既存の受信者にメールを送信します。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-139">An entry is modified by sending mail to an existing recipient in the list.</span></span>
    
- <span data-ttu-id="4d5cf-140">UI を通じてユーザーが、エントリが削除されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-140">An entry is removed by the user through the UI.</span></span>
    
- <span data-ttu-id="4d5cf-141">このトピックに関係のない小さなシナリオです。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-141">Other minor scenarios not relevant to this topic.</span></span>
    
<span data-ttu-id="4d5cf-142">オートコンプリートのデータに変更を保存するには、[オートコンプリートのストリーム](autocomplete-stream.md)にメモリ内構造の書き戻しが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-142">Saving changes to the autocomplete data involves writing the in-memory structure back to an [Autocomplete Stream](autocomplete-stream.md).</span></span> <span data-ttu-id="4d5cf-143">Outlook 2007 との対話、ストリームは、ローカル .nk2 ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-143">When interacting with Outlook 2007, the stream is saved to a local .nk2 file.</span></span> <span data-ttu-id="4d5cf-144">Outlook 2010 または Outlook 2013 では、オートコンプリートのストリームに書き込みます、メール アカウントの配信ストアの受信トレイの内容を関連付けられているテーブル。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-144">For Outlook 2010 or Outlook 2013, the autocomplete stream writes back to the Associated Contents table of the Inbox of the mail account's delivery store.</span></span>
  
## <a name="recommendations"></a><span data-ttu-id="4d5cf-145">推奨事項</span><span class="sxs-lookup"><span data-stu-id="4d5cf-145">Recommendations</span></span>

- <span data-ttu-id="4d5cf-146">決して部分的にオートコンプリートのストリームを変更します。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-146">Never partially modify the autocomplete stream.</span></span> <span data-ttu-id="4d5cf-147">1) 全体のオートコンプリートのストリームをメモリに読み込む、2) 構造を変更、メモリ、および 3) 全体のストリームに書き込みますか、メール アカウントの配信ストアの受信トレイの内容を関連付けられているテーブルには、サポートされている操作 (Outlook 2010 またはOutlook 2013) またはローカル .nk2 ファイル (Outlook 2007)。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-147">The supported interaction is to 1) read the entire autocomplete stream into memory, 2) modify the memory structure, and 3) write the entire stream back to either the Associated Contents table of the Inbox of the mail account's delivery store (for Outlook 2010 or Outlook 2013) or to the local .nk2 file (Outlook 2007).</span></span>
    
- <span data-ttu-id="4d5cf-148">対話せず、オートコンプリート ストリーム Outlook の実行中にします。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-148">Do not interact with the autocomplete stream while Outlook is running.</span></span> <span data-ttu-id="4d5cf-149">ストリームを変更するときに Outlook が実行中の場合、シャット ダウン時、変更内容が上書きされます可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-149">If Outlook is running while you modify the stream, it will likely overwrite your changes when it shuts down.</span></span>
    
- <span data-ttu-id="4d5cf-150">操作を行いますしない書き込み] のプロパティ PT_MV_UNICODE および PR_MV_STRING8 Microsoft Outlook 2003 が使用するオートコンプリート ストリームにします。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-150">Do not write properties of type PT_MV_UNICODE and PR_MV_STRING8 into an autocomplete stream to be consumed by Microsoft Outlook 2003.</span></span> <span data-ttu-id="4d5cf-151">これらのプロパティは、Outlook 2007 と Outlook 2010、Outlook 2013 でのみ認識されます。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-151">These properties are only understood by Outlook 2007, Outlook 2010, and Outlook 2013.</span></span>
    
- <span data-ttu-id="4d5cf-152">読み書きしている標準的なファイル ・ ロック ・ (たとえば、**ロック ファイル**で C または C++ および**の Api を使用してその中に他のプロセスによって変更から .nk2 ファイルをロックすることをお勧めして Outlook 2007 を操作するコードを開発する場合FileStream.Lock**では C#)。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-152">When developing code that interacts with Outlook 2007, we recommend that you lock the .nk2 file from modification by other processes while you are reading and writing it using standard file locking APIs (for example, **LockFile** in C/C++ and **FileStream.Lock** in C#).</span></span> 
    
- <span data-ttu-id="4d5cf-153">オートコンプリート ストリームの行セットからの型のプロパティを変更するだけです。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-153">Only modify the properties of types that are from the row-set of the autocomplete stream.</span></span> <span data-ttu-id="4d5cf-154">オートコンプリートのストリームのプロパティとプロパティの型の詳細については、[オートコンプリートのストリーム](autocomplete-stream.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d5cf-154">For more information about the autocomplete stream properties and property types, see [Autocomplete Stream](autocomplete-stream.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d5cf-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="4d5cf-155">See also</span></span>



[<span data-ttu-id="4d5cf-156">オートコンプリート ストリーム</span><span class="sxs-lookup"><span data-stu-id="4d5cf-156">Autocomplete Stream</span></span>](autocomplete-stream.md)
  
[<span data-ttu-id="4d5cf-157">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="4d5cf-157">MAPI Profiles</span></span>](mapi-profiles.md)


[<span data-ttu-id="4d5cf-158">Outlook 2003/2007 の NK2 ファイル形式と開発者のガイドライン</span><span class="sxs-lookup"><span data-stu-id="4d5cf-158">Outlook 2003/2007 NK2 File Format and Developer Guidelines</span></span>](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)


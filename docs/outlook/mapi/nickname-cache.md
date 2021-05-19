---
title: ニックネーム キャッシュ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: '最終更新日: 2013 年 1 月 30 日'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334518"
---
# <a name="nickname-cache"></a><span data-ttu-id="21460-103">ニックネーム キャッシュ</span><span class="sxs-lookup"><span data-stu-id="21460-103">Nickname cache</span></span>

 
  
<span data-ttu-id="21460-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21460-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21460-105">Microsoft Office Outlook 2007、Microsoft Outlook 2010、Microsoft Outlook 2013は、"オートコンプリート ストリーム" とも呼ばれるニックネーム キャッシュと対話します。</span><span class="sxs-lookup"><span data-stu-id="21460-105">Microsoft Office Outlook 2007, Microsoft Outlook 2010, and Microsoft Outlook 2013 interact with the nickname cache, also known as the "autocomplete stream."</span></span> <span data-ttu-id="21460-106">オートコンプリート ストリームは、Outlook がオートコンプリート リストを保持する場所です。これは、ユーザーが電子メールを作成している間、To、Cc、および **Bcc** の編集ボックスに表示される名前の一覧です。  </span><span class="sxs-lookup"><span data-stu-id="21460-106">The autocomplete stream is where Outlook persists the autocomplete list, which is the list of names that displays in the **To**, **Cc**, and **Bcc** edit boxes while a user is composing an email.</span></span> <span data-ttu-id="21460-107">このトピックでは、Outlook 2007、Outlook 2010、Outlook 2013 がオートコンプリート ストリームとやり取りする方法と、ファイルのバイナリ形式とオートコンプリート ストリームを操作するための推奨される方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="21460-107">This topic describes how Outlook 2007, Outlook 2010, and Outlook 2013 interact with the autocomplete stream and also discusses the binary format of the file and the recommended ways for interacting with the autocomplete stream.</span></span> 
  
<span data-ttu-id="21460-108">Outlook 2010 または Outlook 2013 と対話するアプリケーションの場合、オートコンプリート ストリームは MAPI プロパティとして格納され、MAPI またはメッセージの **PropertyAccessor** オブジェクトを使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="21460-108">For applications that interact with Outlook 2010 or Outlook 2013, the autocomplete stream is stored as a MAPI property and can be modified using the MAPI or the **PropertyAccessor** object of the message.</span></span> <span data-ttu-id="21460-109">**PropertyAccessor オブジェクト** は、2010 年または 2013 Outlook 2013 Outlookで公開されます。</span><span class="sxs-lookup"><span data-stu-id="21460-109">The **PropertyAccessor** object is exposed in the Outlook 2010 or Outlook 2013 object models.</span></span> 
  
<span data-ttu-id="21460-110">2007 オブジェクト モデルOutlook MAPI API には依存関係はありません。</span><span class="sxs-lookup"><span data-stu-id="21460-110">There are no dependencies on the Outlook 2007 object model or MAPI APIs.</span></span> <span data-ttu-id="21460-111">したがって、2007 年から 2007 年Outlookでオートコンプリート ストリームに変更を加えるアプリケーションは、任意のプログラミング言語を使用して記述できます。</span><span class="sxs-lookup"><span data-stu-id="21460-111">Therefore, applications that make changes to the autocomplete stream within Outlook 2007 can be written using any programming language.</span></span>
  
## <a name="interacting-with-the-autocomplete-stream"></a><span data-ttu-id="21460-112">オートコンプリート ストリームの操作</span><span class="sxs-lookup"><span data-stu-id="21460-112">Interacting with the Autocomplete Stream</span></span>

<span data-ttu-id="21460-113">メッセージで **[To]** **、Cc、\*\*\*\*または Bcc** の編集ボックスにアクセスすると、オートコンプリート ストリームが読み込まれ、ユーザー名の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="21460-113">When the **To**, **Cc**, or **Bcc** edit boxes are accessed on a message, the autocomplete stream is loaded and the list of user names is displayed.</span></span> <span data-ttu-id="21460-114">Outlookオートコンプリート ストリームを操作するには、次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="21460-114">Outlook interacts with the autocomplete stream in two ways:</span></span> 
  
1. <span data-ttu-id="21460-115">オートコンプリート ストリームの読み込み</span><span class="sxs-lookup"><span data-stu-id="21460-115">Loading the autocomplete stream</span></span> 
    
2. <span data-ttu-id="21460-116">オートコンプリート ストリームのデータに対する変更の保存</span><span class="sxs-lookup"><span data-stu-id="21460-116">Saving changes to the data in the autocomplete stream</span></span>
    
<span data-ttu-id="21460-117">オートコンプリート データを格納する方法は、Outlook 2007 と Outlook 2010 または Outlook 2013 の間で異なります。</span><span class="sxs-lookup"><span data-stu-id="21460-117">The means of storing the autocomplete data differs between Outlook 2007 and Outlook 2010 or Outlook 2013 as follows:</span></span> 
  
 <span data-ttu-id="21460-118">**Outlook 2007**</span><span class="sxs-lookup"><span data-stu-id="21460-118">**Outlook 2007**</span></span>
  
<span data-ttu-id="21460-119">2007 Outlook、オートコンプリート ストリームはプロファイルと同じ名前で拡張子 .nk2 のファイルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="21460-119">For Outlook 2007, the autocomplete stream is stored in a file with the same name as the profile and an extension of .nk2.</span></span> <span data-ttu-id="21460-120">たとえば、"outlook" の既定のプロファイルを使用する場合、ファイルは "outlook.nk2" と呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="21460-120">For example, if the default profile of "outlook" is used, the file will be called "outlook.nk2".</span></span> <span data-ttu-id="21460-121">.nk2 ファイルは %APPDATA%\Microsoft\Outlook に格納されます。</span><span class="sxs-lookup"><span data-stu-id="21460-121">The .nk2 file is stored in %APPDATA%\Microsoft\Outlook.</span></span> <span data-ttu-id="21460-122">ニックネーム キャッシュ バイナリ ファイル形式の詳細については[、「Outlook NK2](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)ファイル形式と開発者向けガイドライン」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21460-122">For more information about the nickname cache binary file format, see [Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).</span></span>
  
 <span data-ttu-id="21460-123">**Outlook 2010 および Outlook 2013**</span><span class="sxs-lookup"><span data-stu-id="21460-123">**Outlook 2010 and Outlook 2013**</span></span>
  
<span data-ttu-id="21460-124">Outlook 2010 または Outlook 2013 は、メール アカウントの配信ストアの受信トレイの [関連コンテンツ] テーブルにあるメッセージからオートコンプリート ストリームを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="21460-124">Outlook 2010 or Outlook 2013 reads the autocomplete stream from a message in the Associated Contents table of the Inbox of the mail account's delivery store.</span></span> <span data-ttu-id="21460-125">この非表示のメッセージには、メッセージ クラスと、メッセージのIPM.Configがあります。オートコンプリート。</span><span class="sxs-lookup"><span data-stu-id="21460-125">This hidden message has a message class and subject of IPM.Configuration.Autocomplete.</span></span> <span data-ttu-id="21460-126">オートコンプリート ストリームは、PR_ROAMING_BINARYSTREAM プロパティ[(PidTagRoamingBinary 標準](pidtagroamingbinary-canonical-property.md)プロパティ) のこのメッセージに格納されます。</span><span class="sxs-lookup"><span data-stu-id="21460-126">The autocomplete stream is stored on this message in the PR_ROAMING_BINARYSTREAM property ([PidTagRoamingBinary Canonical Property](pidtagroamingbinary-canonical-property.md)).</span></span> <span data-ttu-id="21460-127">オートコンプリート データは、%USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache にあるオートコンプリート .dat ファイルに一時的にキャッシュされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="21460-127">The autocomplete data may be temporarily cached in an autocomplete .dat file located in %USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache.</span></span> <span data-ttu-id="21460-128">ただし、.dat ファイルはキャッシュのみであり、ユーザーが 2010 年または 2013 年 2013 年に終了した場合、配信ストアに書きOutlookにはOutlookされません。</span><span class="sxs-lookup"><span data-stu-id="21460-128">However, the .dat file is only a cache and is not used to write back to the delivery store when the user exits Outlook 2010 or Outlook 2013.</span></span>
  
## <a name="loading-the-autocomplete-stream"></a><span data-ttu-id="21460-129">オートコンプリート ストリームの読み込み</span><span class="sxs-lookup"><span data-stu-id="21460-129">Loading the Autocomplete Stream</span></span>

<span data-ttu-id="21460-130">Outlook機能を持つアイテムが初期化されるたびに、オートコンプリート ストリームが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="21460-130">Outlook loads the autocomplete stream whenever an item with addressing functionality is initialized.</span></span> <span data-ttu-id="21460-131">たとえば、電子メール アドレスは、新しいメール、メール返信、連絡先アイテム、会議出席依頼などで使用されます。</span><span class="sxs-lookup"><span data-stu-id="21460-131">For example, email addresses are used in a new mail, a mail reply, a contact item, a meeting request, and so on.</span></span> <span data-ttu-id="21460-132">データを読み込むOutlookストリームのすべての内容をメモリに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="21460-132">To load the data, Outlook reads all of the contents of the stream into memory.</span></span>
  
<span data-ttu-id="21460-133">オートコンプリート操作の場合、Outlookプロセスの有効期間の間、このメモリ内構造outlook.exe対話します。</span><span class="sxs-lookup"><span data-stu-id="21460-133">For autocomplete operations, Outlook interacts exclusively with this in-memory structure for the duration of the outlook.exe process lifetime.</span></span> <span data-ttu-id="21460-134">Outlookシャットダウン時にのみ構造が保存されます。</span><span class="sxs-lookup"><span data-stu-id="21460-134">Outlook only saves the structure on shutdown.</span></span> <span data-ttu-id="21460-135">このプロセスの詳細については、次のセクション「オートコンプリート ストリームの保存」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21460-135">See the following section "Saving the Autocomplete Stream" for more information on this process.</span></span>
  
## <a name="saving-the-autocomplete-stream"></a><span data-ttu-id="21460-136">オートコンプリート ストリームの保存</span><span class="sxs-lookup"><span data-stu-id="21460-136">Saving the Autocomplete Stream</span></span>

<span data-ttu-id="21460-137">Outlookオートコンプリート リストが次の方法で変更された場合、オートコンプリート ストリームはシャットダウン時に保存されます。</span><span class="sxs-lookup"><span data-stu-id="21460-137">Outlook saves the autocomplete stream on shutdown if the autocomplete list has changed in any of the following ways:</span></span>
  
- <span data-ttu-id="21460-138">新しいニックネーム エントリは、名前の解決、アドレス帳ダイアログから受信者の選択、またはリストに未登録の受信者へのメールの送信を通じて追加されます。</span><span class="sxs-lookup"><span data-stu-id="21460-138">A new nickname entry is added through resolving a name, picking a recipient from the address book dialog, or sending mail to a recipient that was not already in the list.</span></span>
    
- <span data-ttu-id="21460-139">エントリは、リスト内の既存の受信者にメールを送信することで変更されます。</span><span class="sxs-lookup"><span data-stu-id="21460-139">An entry is modified by sending mail to an existing recipient in the list.</span></span>
    
- <span data-ttu-id="21460-140">UI を使用してユーザーがエントリを削除します。</span><span class="sxs-lookup"><span data-stu-id="21460-140">An entry is removed by the user through the UI.</span></span>
    
- <span data-ttu-id="21460-141">このトピックに関連しないその他の小さなシナリオ。</span><span class="sxs-lookup"><span data-stu-id="21460-141">Other minor scenarios not relevant to this topic.</span></span>
    
<span data-ttu-id="21460-142">オートコンプリート データへの変更を保存するには、メモリ内構造をオートコンプリート ストリームに書 [き戻す必要があります](autocomplete-stream.md)。</span><span class="sxs-lookup"><span data-stu-id="21460-142">Saving changes to the autocomplete data involves writing the in-memory structure back to an [Autocomplete Stream](autocomplete-stream.md).</span></span> <span data-ttu-id="21460-143">2007 Outlook操作すると、ストリームはローカルの .nk2 ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="21460-143">When interacting with Outlook 2007, the stream is saved to a local .nk2 file.</span></span> <span data-ttu-id="21460-144">2010 Outlook Outlook 2013 の場合、オートコンプリート ストリームはメール アカウントの配信ストアの受信トレイの [関連コンテンツ] テーブルに書き戻されます。</span><span class="sxs-lookup"><span data-stu-id="21460-144">For Outlook 2010 or Outlook 2013, the autocomplete stream writes back to the Associated Contents table of the Inbox of the mail account's delivery store.</span></span>
  
## <a name="recommendations"></a><span data-ttu-id="21460-145">推奨事項</span><span class="sxs-lookup"><span data-stu-id="21460-145">Recommendations</span></span>

- <span data-ttu-id="21460-146">オートコンプリート ストリームを部分的に変更しない。</span><span class="sxs-lookup"><span data-stu-id="21460-146">Never partially modify the autocomplete stream.</span></span> <span data-ttu-id="21460-147">サポートされる操作は、1) オートコンプリート ストリーム全体をメモリに読み取り、2) メモリ構造を変更し、3) ストリーム全体をメール アカウントの配信ストアの受信トレイの [関連コンテンツ] テーブル (Outlook 2010 または Outlook 2013) またはローカルの .nk2 ファイル (Outlook 2007) に書き戻します。</span><span class="sxs-lookup"><span data-stu-id="21460-147">The supported interaction is to 1) read the entire autocomplete stream into memory, 2) modify the memory structure, and 3) write the entire stream back to either the Associated Contents table of the Inbox of the mail account's delivery store (for Outlook 2010 or Outlook 2013) or to the local .nk2 file (Outlook 2007).</span></span>
    
- <span data-ttu-id="21460-148">ユーザーが実行中にオートコンプリート ストリームOutlook操作しない。</span><span class="sxs-lookup"><span data-stu-id="21460-148">Do not interact with the autocomplete stream while Outlook is running.</span></span> <span data-ttu-id="21460-149">ストリームOutlook実行中は、変更がシャットダウン時に上書きされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="21460-149">If Outlook is running while you modify the stream, it will likely overwrite your changes when it shuts down.</span></span>
    
- <span data-ttu-id="21460-150">Microsoft PT_MV_UNICODE 2003 PR_MV_STRING8で使用されるオートコンプリート ストリームには、Outlookを記述Outlook。</span><span class="sxs-lookup"><span data-stu-id="21460-150">Do not write properties of type PT_MV_UNICODE and PR_MV_STRING8 into an autocomplete stream to be consumed by Microsoft Outlook 2003.</span></span> <span data-ttu-id="21460-151">これらのプロパティは、2007 年Outlook 2010 年Outlook 2013 年Outlookのみです。</span><span class="sxs-lookup"><span data-stu-id="21460-151">These properties are only understood by Outlook 2007, Outlook 2010, and Outlook 2013.</span></span>
    
- <span data-ttu-id="21460-152">Outlook 2007 と対話するコードを開発する場合は、標準のファイル ロック API (C/C++ の **LockFile、C#** の **FileStream.Lock** など) を使用して読み取りおよび書き込み中に、.nk2 ファイルを他のプロセスによる変更からロックすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="21460-152">When developing code that interacts with Outlook 2007, we recommend that you lock the .nk2 file from modification by other processes while you are reading and writing it using standard file locking APIs (for example, **LockFile** in C/C++ and **FileStream.Lock** in C#).</span></span> 
    
- <span data-ttu-id="21460-153">オートコンプリート ストリームの行セットからの型のプロパティのみを変更します。</span><span class="sxs-lookup"><span data-stu-id="21460-153">Only modify the properties of types that are from the row-set of the autocomplete stream.</span></span> <span data-ttu-id="21460-154">オートコンプリート ストリームのプロパティとプロパティの種類の詳細については [、「Autocomplete Stream」を参照してください](autocomplete-stream.md)。</span><span class="sxs-lookup"><span data-stu-id="21460-154">For more information about the autocomplete stream properties and property types, see [Autocomplete Stream](autocomplete-stream.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21460-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="21460-155">See also</span></span>



[<span data-ttu-id="21460-156">オートコンプリート ストリーム</span><span class="sxs-lookup"><span data-stu-id="21460-156">Autocomplete Stream</span></span>](autocomplete-stream.md)
  
[<span data-ttu-id="21460-157">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="21460-157">MAPI Profiles</span></span>](mapi-profiles.md)


[<span data-ttu-id="21460-158">Outlook 2003/2007 NK2 ファイル形式と開発者向けガイドライン</span><span class="sxs-lookup"><span data-stu-id="21460-158">Outlook 2003/2007 NK2 File Format and Developer Guidelines</span></span>](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)


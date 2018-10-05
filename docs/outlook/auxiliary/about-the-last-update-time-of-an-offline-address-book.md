---
title: オフライン アドレス帳の最終更新時刻について
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d8c554c5-89ac-9b32-5561-8d8178d2525a
description: オフライン アドレス帳 (OAB) は、Outlook ユーザーが、切断された状態情報にアクセスできるディレクトリからグローバル アドレス一覧 (GAL) およびその他のアドレス帳からを提供します。
ms.openlocfilehash: 3374f87cd62d46a80ed823bff0516115a58c155c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392285"
---
# <a name="about-the-last-update-time-of-an-offline-address-book"></a><span data-ttu-id="d36fb-103">オフライン アドレス帳の最終更新時刻について</span><span class="sxs-lookup"><span data-stu-id="d36fb-103">About the last update time of an Offline Address Book</span></span>

<span data-ttu-id="d36fb-p101">オフライン アドレス帳 (OAB) は、Outlook ユーザーが、切断された状態情報にアクセスできるディレクトリからグローバル アドレス一覧 (GAL) およびその他のアドレス帳からを提供します。Outlook がオフラインのアクセスを提供する Exchange サーバーからダウンロードするアドレス帳のコピーすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d36fb-p101">An Offline Address Book (OAB) provides Outlook users in a disconnected state access to directory information from the Global Address List (GAL) and from other address books. It is a copy of an Address Book that Outlook has downloaded from an Exchange server to provide offline access.</span></span>
  
<span data-ttu-id="d36fb-p102">Exchange 管理者は、ユーザーがオフラインで作業できるようにするには、どのアドレス帳を選択できます。アドレス帳のコピーを作成するには、Exchange は、ファイルを圧縮、および、ローカル共有に配置する新しい OAB ファイルが生成されます。Outlook の構成方法によっては、Outlook は、切断された状態で Web サイトからまたはクライアント コンピューターにパブリック フォルダーのいずれかを使用して OAB ファイルをダウンロードします。Outlook は定期的にチェックされ、更新された OAB がダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="d36fb-p102">Exchange administrators can choose which Address Books to make available for users who work offline. To create a copy of an Address Book, Exchange generates new OAB files, compresses the files, and places them on a local share. Depending on how Outlook is configured, Outlook downloads the OAB files either from the Web or from a Public Folder to a client computer for use in a disconnected state. Outlook periodically checks for and downloads OAB updates.</span></span>
  
<span data-ttu-id="d36fb-p103">ユーザーの OAB へのオフライン アクセスを提供する outlook ソリューションでは、OAB が Exchange サーバーから最後に更新されたときに検出する必要があります。 OAB の最終更新時刻を検索するには、ソリューションは、Windows レジストリで次のエントリを使用できます: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB 最終変更時間** 。このレジストリ エントリの種類は、 **REG_BINARY** です。データは、サイズが 8 バイトです。前回ダウンロードされた OAB ファイルの Exchange サーバーからクライアント コンピューターに世界協定時刻 (UTC) の値を指定する 64 ビット [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx)構造体にデータを変換できます。</span><span class="sxs-lookup"><span data-stu-id="d36fb-p103">Outlook solutions that want to provide their users offline access to an OAB may need to find out when the OAB was last updated from the Exchange server. To find the last update time of an OAB, solutions can use the following entry in the Windows registry: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB Last Modified Time**. The type of this registry entry is **REG_BINARY**. The data is 8 bytes in size. You can convert the data to a 64-bit [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) structure specifying a Universal Coordinated Time (UTC) value that Outlook last downloaded the OAB files from the Exchange server to the client computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d36fb-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="d36fb-115">See also</span></span>

- [<span data-ttu-id="d36fb-116">Managing Offline Address Books</span><span class="sxs-lookup"><span data-stu-id="d36fb-116">Managing Offline Address Books</span></span>](https://msdn.microsoft.com/library/b7f26eca-b93b-4834-ba50-11febdefbb18.aspx)


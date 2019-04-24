---
title: コンピューター上で Outlook がクイック実行アプリケーションかどうかを確認する
TOCTitle: Determine whether Outlook is a Click-to-Run application on a computer
ms:assetid: 1b8573be-8ea8-4973-869d-87fda57ce525
ms:mtpsurl: https://msdn.microsoft.com/library/Ff522355(v=office.15)
ms:contentKeyID: 55119804
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a710baa4d70ac69b67d2a06fe694998884fd835
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356407"
---
# <a name="determine-whether-outlook-is-a-click-to-run-application-on-a-computer"></a><span data-ttu-id="3e8fa-102">コンピューター上で Outlook がクイック実行アプリケーションかどうかを確認する</span><span class="sxs-lookup"><span data-stu-id="3e8fa-102">Determine whether Outlook is a Click-to-Run application on a computer</span></span>

<span data-ttu-id="3e8fa-p101">クイック実行は、Office 2010 以降のバージョンで利用できるソフトウェアの配信と更新のメカニズムです。クイック実行で配信された製品は、ローカル オペレーティング システム上の仮想アプリケーション環境で実行されます。つまり、それらの製品は独自のファイルと設定のプライベート コピーを持ち、それらが行った変更は仮想環境内に格納されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fa-p101">Click-to-Run is a software delivery and updating mechanism available to Office 2010 and later versions. Products delivered via Click-to-Run execute in a virtual application environment on the local operating system. This means that they have private copies of their files and settings, and that any changes they make are captured in the virtual environment.</span></span>

<span data-ttu-id="3e8fa-106">クイック実行は高速です。ユーザーは、製品全体のインストールが完了するまで待機することなく、短時間のうちにアプリケーションの実行を開始できます。</span><span class="sxs-lookup"><span data-stu-id="3e8fa-106">Click-to-Run is fast—users can start running an application within a short time without waiting for the complete product to finish installing.</span></span> <span data-ttu-id="3e8fa-107">更新プログラムはバックグラウンドで自動的に実行されます。ユーザーが、最初にインストールを削除する必要や、手動で更新プログラムをインストールする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3e8fa-107">Updates are run automatically in the background, without requiring a user to first remove an installation or manually install updates.</span></span> <span data-ttu-id="3e8fa-108">クイック実行の製品は仮想化されていて、インストール済みの別のソフトウェアと競合することはありません。</span><span class="sxs-lookup"><span data-stu-id="3e8fa-108">Click-to-Run products are virtualized and do not conflict with other installed software.</span></span> <span data-ttu-id="3e8fa-109">ただし、クイック実行で配信される製品には、その製品のすべてのファイルと登録のプライベート コピーがあるため、アドインの開発者は、クライアント コンピューターのハード ディスクにインストールされていた製品と同じ方法では、その製品が存在しているかどうかを判断できません。</span><span class="sxs-lookup"><span data-stu-id="3e8fa-109">However, because a product delivered by Click-to-Run has private copies of all its files and registration, an add-in developer cannot determine the product’s existence in the same manner as a product that was installed on a client computer’s hard disk.</span></span> <span data-ttu-id="3e8fa-110">Outlook 2010 以降、アドインの開発者は、Outlook がインストールされているかどうかと、Outlook がクイック実行製品として配信されたものかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fa-110">Starting with Outlook 2010, add-in developers should verify whether Outlook has been installed, and whether Outlook has been delivered as a Click-to-Run product.</span></span>


> [!NOTE]
> <span data-ttu-id="3e8fa-111">[!メモ] クイック実行仮想アプリケーション環境でサポートされるのは 32 ビットの Office 2013 だけです。このことは、クライアント コンピューターで 64 ビットのオペレーティング システムを実行しているとしても変わりません。</span><span class="sxs-lookup"><span data-stu-id="3e8fa-111">Only 32-bit Office 2013 is supported in the Click-to-Run virtual application environment, even if the client computer runs a 64-bit operating system.</span></span>



### <a name="to-check-whether-outlook-2013-was-delivered-by-click-to-run-on-a-client-computer"></a><span data-ttu-id="3e8fa-112">Outlook 2013 がクイック実行でクライアント コンピューターに配信されたものかどうかを確認するには</span><span class="sxs-lookup"><span data-stu-id="3e8fa-112">To check whether Outlook 2013 was delivered by Click-to-Run on a client computer</span></span>

- <span data-ttu-id="3e8fa-113">Windows レジストリ内の次の場所に VirtualOutlook キーが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="3e8fa-113">Verify whether the VirtualOutlook key exists in the following location in the Windows registry:</span></span>
    
  `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
    
  <span data-ttu-id="3e8fa-114">VirtualOutlook キーは REG\_SZ 値です。この値には、インストールされている製品の言語のカルチャ タグ ("en-us" など) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3e8fa-114">The VirtualOutlook key is a REG\_SZ value that contains the culture tag of the installed product language, such as "en-us".</span></span>

## <a name="see-also"></a><span data-ttu-id="3e8fa-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e8fa-115">See also</span></span>

- [<span data-ttu-id="3e8fa-116">アドイン管理</span><span class="sxs-lookup"><span data-stu-id="3e8fa-116">Add-in administration</span></span>](add-in-administration.md)


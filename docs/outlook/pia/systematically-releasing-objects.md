---
title: オブジェクトを系統的に解放する
TOCTitle: Systematically releasing objects
ms:assetid: d4cd1d8e-aae6-483b-a4d8-1656171e838d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623945(v=office.15)
ms:contentKeyID: 55119785
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 812f720b3ebab1100040802d7593548063497297
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406835"
---
# <a name="systematically-releasing-objects"></a><span data-ttu-id="1e3e0-102">オブジェクトを系統的に解放する</span><span class="sxs-lookup"><span data-stu-id="1e3e0-102">Systematically Releasing Objects</span></span>

<span data-ttu-id="1e3e0-p101">このトピックでは、Outlook を使用するアドイン開発者と IT 管理者向けに、アドインをシャットダウンするときの推奨事項を要約します。詳細については、「[Outlook 2010 でのシャットダウンの変更](https://msdn.microsoft.com/library/ee720183\(v=office.15\))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-p101">This topic summarizes add-in shutdown recommendations for add-in developers and IT administrators that use Outlook. For more information, see [Shutdown Changes for Outlook 2010](https://msdn.microsoft.com/library/ee720183\(v=office.15\)).</span></span>

## <a name="add-in-shutdown-changes-in-outlook"></a><span data-ttu-id="1e3e0-105">Outlook アドインのシャットダウンの変更</span><span class="sxs-lookup"><span data-stu-id="1e3e0-105">Add-in Shutdown Changes in Outlook</span></span>

<span data-ttu-id="1e3e0-106">Outlook 2010 以降の Outlook は、既定ではシャットダウンしているアドインを通知しません。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-106">Starting in Outlook 2010, Outlook, by default, does not signal add-ins that it is shutting down.</span></span> <span data-ttu-id="1e3e0-107">具体的には、Outlook は、高速シャットダウン時に **IDTExtensibility2** インターフェイスの **OnBeginShutdown(Array)** メソッドおよび **OnDisconnection(ext\_DisconnectMode, Array)** メソッドを呼び出さなくなりました。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-107">Specifically, Outlook no longer calls the **OnBeginShutdown(Array)** and **OnDisconnection(ext_DisconnectMode, Array)** methods of the **IDTExtensibility2** interface during fast shutdown.</span></span> <span data-ttu-id="1e3e0-108">同様に、Visual Studio 2010 以降のバージョンの Office 開発ツールで作成した Outlook アドインは、Outlook のシャットダウン中に ThisAddin\_Shutdown メソッドを呼び出さなくなりました。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-108">Similarly, an Outlook add-in, written with Office development tools in Visual Studio 2010 or a later version, no longer calls the \_ method when Outlook is shutting down.</span></span> 

<span data-ttu-id="1e3e0-109">これらのメソッドを呼び出さなくなったのは、シャットダウン時に大多数のアドインは参照の解放のような単純なタスクを実行する一方、Web サービスやその他の比較的実行時間の長い処理を同期的に呼び出すアドインも存在するため、Outlook のシャットダウンがかなり遅れることがあったからです。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-109">The reason to stop calling these methods is that while a majority of add-ins perform simple tasks like releasing references, some add-ins make Web service calls or other long-running operations synchronously during these events, significantly delaying Outlook from shutting down.</span></span> <span data-ttu-id="1e3e0-110">この変更の結果として、シャットダウン時の動作が以前の Outlook よりも向上しました。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-110">As a result of this change, Outlook works better than it has in the past when shutting down.</span></span>

## <a name="recommendations-for-add-in-shutdown-for-developers"></a><span data-ttu-id="1e3e0-111">アドインのシャットダウンに関する開発者向けの推奨事項</span><span class="sxs-lookup"><span data-stu-id="1e3e0-111">Recommendations for Add-in Shutdown for Developers</span></span>

<span data-ttu-id="1e3e0-112">エンド ユーザーが Outlook の高速で応答性の高いシャットダウンを今後も享受できるようにするため、開発者は以下の推奨事項に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-112">It is important that developers observe the following recommendations for add-in shutdown to ensure that end users continue to benefit from a fast and responsive Outlook shutdown experience.</span></span>

- <span data-ttu-id="1e3e0-113">アドインには、これまでどおりに OnBeginShutdown メソッドと OnDisconnection メソッドまたは ThisAddin\_Shutdown を実装して、参照と割り当てられたメモリを解放するようにしてください。これは、管理者がグループ ポリシーを通じて低速シャットダウンに戻すことや、ユーザーが **[COM アドイン]** ダイアログ ボックスから手動でアドインを切断することがあるためです。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-113">Add-ins should continue to implement the OnBeginShutdown and OnDisconnection methods or ThisAddin_Shutdown to release references and allocated memory, because there are scenarios in which administrators might revert to slow shutdown through group policy, or the user might manually disconnect your add-in through the COM Add-ins dialog box.</span></span>

- <span data-ttu-id="1e3e0-114">アドイン開発者は、シャットダウン中に絶対に必要になるタスクのみを実行してください。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-114">Add-in developers should only perform tasks that absolutely must take place during shutdown.</span></span>

- <span data-ttu-id="1e3e0-115">アドイン開発者は、さまざまな状況や、Outlook のシャットダウンを制御するレジストリの設定をいろいろ変えてアドインのパフォーマンスを評価し、Outlook で適切に動作するようにアドインを積極的に修正してください。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-115">Add-in developers should evaluate the performance of their add-ins in various scenarios and under different Windows registry settings that control Outlook shutdown, and proactively modify their add-ins to work with Outlook.</span></span>

## <a name="recommendations-for-add-in-shutdown-for-it-administrators"></a><span data-ttu-id="1e3e0-116">アドインのシャットダウンに関する IT 管理者向けの推奨事項</span><span class="sxs-lookup"><span data-stu-id="1e3e0-116">Recommendations for Add-in Shutdown for IT Administrators</span></span>

<span data-ttu-id="1e3e0-117">IT 管理者は、既に企業内に展開しているアドインを Outlook の新しいシャットダウン機構と合致するようにアップグレードできない場合、Windows のレジストリの設定をいくつか変更すれば、低速シャットダウンの動作に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-117">For IT administrators, if there are add-ins that are already deployed in an enterprise and cannot be upgraded to become compatible with the new shutdown Outlook mechanism, IT administrators can resort to a couple of Windows registry settings to revert to the slow shutdown behavior.</span></span>

### <a name="individual-add-in-setting"></a><span data-ttu-id="1e3e0-118">アドインの個別設定</span><span class="sxs-lookup"><span data-stu-id="1e3e0-118">Individual Add-in Setting</span></span>

<span data-ttu-id="1e3e0-p104">IT 管理者は、アドインの展開の一部として、個別の Outlook アドインへのシャットダウン通知を有効にできます。グループ ポリシーを使用してこれを行うことはできませんが、特定のアドインについて下位互換性が必要な場合に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-p104">IT administrators can enable shutdown notifications to individual Outlook add-ins as part of the add-in deployment. Although you cannot do this through group policy, it is useful if you have backward-compatibility requirements for specific add-ins.</span></span>

<span data-ttu-id="1e3e0-p105">この設定は、HKCU または HKLM レジストリ ハイブのアドイン登録で、アドインごとにアドイン登録に値を追加して構成してください。次のテキストを 1 行で入力します。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-p105">Configure this setting for each add-in through the add-in registration in the HKCU or the HKLM registry hives, by adding an additional value to the add-in registration. Type the following text as a single line:</span></span>

`HKCU\Software\Microsoft\Office\Outlook\Add-ins\<ProgID>[RequireShutdownNotification]=dword:0x1`

<span data-ttu-id="1e3e0-p106">この値を 0x1 に設定すると、アドインは Outlook のシャットダウン時にブロック コールバックを受け取ることができるようになります。これは Outlook のシャットダウンのパフォーマンスに影響するので、使用すべきかどうかを展開の際に評価するようにしてください。この設定を使用するのは、アドインと新しいシャットダウン機構との適合性が特に問題となる場合に限ってください。この値を 0x0 に設定すると、Outlook の既定の動作が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-p106">Setting this value to 0x1 enables the add-in to receive blocked callbacks during Outlook shutdown. This has an impact on the performance of Outlook shutdown and should be evaluated as part of a deployment. This setting should be used only if an add-in has significant compatibility issues with the new shutdown mechanism. Setting the value to 0x0 uses the default behavior of Outlook.</span></span>

### <a name="global-setting"></a><span data-ttu-id="1e3e0-127">グローバル設定</span><span class="sxs-lookup"><span data-stu-id="1e3e0-127">Global setting</span></span>

<span data-ttu-id="1e3e0-p107">IT 管理者はグループ ポリシーを使用して、すべてのアドインに対するシャットダウン時の通知をまとめて有効にすることができます。この方法は組織に存在する多数の内部ソリューションやデスクトップでこの設定を展開して、Outlook のロールアウト時に矛盾が生じないようにする必要がある場合に推奨されます。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-p107">IT administrators can enable shutdown notifications globally for all add-ins through group policy. This is recommended for organizations that have a large number of internal solutions or desktops that need to deploy this setting to ensure compatibility during a rollout of Outlook.</span></span>

<span data-ttu-id="1e3e0-p108">この設定は、シャットダウン機構の動作を Outlook 2007 と同じにするためのものです。この設定は、ユーザー単位またはコンピューター単位でのグループ ポリシーを通じて、この設定を展開できます。次のテキストを 1 行で入力します。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-p108">Use this setting to change the shutdown mechanism to match that used by Outlook 2007. You can deploy the setting through group policy, either per user or per computer. Type the following text as a single line:</span></span>

`HKCU\Policies\Microsoft\Office\Outlook\15.0\Options\Shutdown[AddinFastShutdownBehavior]=dword:0x1`

<span data-ttu-id="1e3e0-133">AddinFastShutdownBehavior を 0x1 に設定すると、すべてのアドインのシャットダウン通知が有効になります。この値を 0x0 に設定すると、Outlook の既定の動作が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1e3e0-133">Setting   to 0x1 enables shutdown notifications for all add-ins. Setting the value to 0x0 uses the default behavior of Outlook.</span></span>


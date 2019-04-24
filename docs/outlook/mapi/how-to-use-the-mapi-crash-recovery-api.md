---
title: MAPI クラッシュ回復 API を使用する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: a73889982e4aa72fb664a8eafd6fc8704e581e98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346425"
---
# <a name="use-the-mapi-crash-recovery-api"></a><span data-ttu-id="bce40-103">MAPI クラッシュ回復 API を使用する</span><span class="sxs-lookup"><span data-stu-id="bce40-103">Use the MAPI Crash Recovery API</span></span>

<span data-ttu-id="bce40-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bce40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bce40-105">このトピックには、C++ のコードサンプルが含まれています。このコードは、[アン handledexceptionfilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx)関数から[mapicrashrecovery](mapicrashrecovery.md)関数を呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bce40-105">This topic contains a code sample in C++ that shows how to call the [MAPICrashRecovery](mapicrashrecovery.md) function from the [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) function.</span></span> <span data-ttu-id="bce40-106">[mapicrashrecovery](mapicrashrecovery.md)関数は、個人用フォルダーファイル (PST) またはオフラインフォルダーファイル (OST) の共有メモリの状態をチェックします。</span><span class="sxs-lookup"><span data-stu-id="bce40-106">The [MAPICrashRecovery](mapicrashrecovery.md) function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> 

<span data-ttu-id="bce40-107">メモリが一貫した状態にある場合、 [mapicrashrecovery](mapicrashrecovery.md)関数はデータをディスクに移動し、プロセスが終了するまで追加の読み取りまたは書き込みアクセスを禁止します。</span><span class="sxs-lookup"><span data-stu-id="bce40-107">If the memory is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> <span data-ttu-id="bce40-108">プロセスが終了する前に、pst または ost が一貫した状態になっていることを確認することにより、microsoft outlook 2010 または microsoft outlook 2013 が次のエラーメッセージを表示しないようにして、パフォーマンスの問題を回避することができます。</span><span class="sxs-lookup"><span data-stu-id="bce40-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2010 or Microsoft Outlook 2013 from displaying the following error message and avoid performance problems:</span></span> 
  
<span data-ttu-id="bce40-109">**データファイルが前回使用され、問題がないかチェックされているときに、データファイルが正常に閉じられませんでした。チェックが進行している間は、パフォーマンスが影響を受ける可能性があります。**</span><span class="sxs-lookup"><span data-stu-id="bce40-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
```cpp
LONG WINAPI UnhandledExceptionFilter(__in EXCEPTION_POINTERS* pep) 
{ 
    // Let the OS terminate the process upon return. 
    LONG retval = EXCEPTION_EXECUTE_HANDLER; 
 
    switch (pep->ExceptionRecord->ExceptionCode) 
    { 
        case EXCEPTION_BREAKPOINT: 
        case EXCEPTION_SINGLE_STEP: 
            // Ignore debugging exceptions. 
            retval = EXCEPTION_CONTINUE_SEARCH; 
            break; 
 
        default: 
            // The process is going to be terminated, so disconnect the MAPI database. 
            MAPICrashRecovery(MAPICRASH_RECOVER); 
            // Optionally, you can display a crash reporting dialog box here. 
            // If the user chooses to debug,  
            // call MAPICrashRecovery(MAPICRASH_CONTINUE). 
            break; 
    } 
 
    return retval; 
}
```

## <a name="see-also"></a><span data-ttu-id="bce40-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="bce40-110">See also</span></span>

- [<span data-ttu-id="bce40-111">MAPI クラッシュ回復 API について</span><span class="sxs-lookup"><span data-stu-id="bce40-111">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md) 
- [<span data-ttu-id="bce40-112">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="bce40-112">MAPICrashRecovery</span></span>](mapicrashrecovery.md)


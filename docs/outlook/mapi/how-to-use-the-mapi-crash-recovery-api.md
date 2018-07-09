---
title: MAPI クラッシュ回復 API を使用します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 8ac75bfb686496c151b5edc3a692c99a6e47ee96
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800264"
---
# <a name="use-the-mapi-crash-recovery-api"></a><span data-ttu-id="c7302-103">MAPI クラッシュ回復 API を使用します。</span><span class="sxs-lookup"><span data-stu-id="c7302-103">Use the MAPI Crash Recovery API</span></span>

<span data-ttu-id="c7302-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7302-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7302-105">このトピックには、 [UnhandledExceptionFilter](http://msdn.microsoft.com/ja-jp/library/ms681401%28VS.85%29.aspx)関数から、 [MAPICrashRecovery](mapicrashrecovery.md)関数を呼び出す方法を示す C++ でのコード サンプルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7302-105">This topic contains a code sample in C++ that shows how to call the [MAPICrashRecovery](mapicrashrecovery.md) function from the [UnhandledExceptionFilter](http://msdn.microsoft.com/ja-jp/library/ms681401%28VS.85%29.aspx) function.</span></span> <span data-ttu-id="c7302-106">[MAPICrashRecovery](mapicrashrecovery.md)関数は、共有メモリを個人用フォルダー ファイル (PST) またはオフライン フォルダー ファイル (OST) の状態をチェックします。</span><span class="sxs-lookup"><span data-stu-id="c7302-106">The [MAPICrashRecovery](mapicrashrecovery.md) function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> 

<span data-ttu-id="c7302-107">メモリは、一貫性のある状態では、 [MAPICrashRecovery](mapicrashrecovery.md)関数はデータをディスクに移動して、プロセスが終了するまでに、さらに読み取りまたは書き込みアクセスを防ぐことが。</span><span class="sxs-lookup"><span data-stu-id="c7302-107">If the memory is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> <span data-ttu-id="c7302-108">ことによって、pst ファイルまたは Ost 整合性の取れた状態でプロセスが終了する前に、Microsoft Outlook 2010 または Microsoft Outlook 2013 が次のエラー メッセージを表示しないようにして、パフォーマンスの問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="c7302-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2010 or Microsoft Outlook 2013 from displaying the following error message and avoid performance problems:</span></span> 
  
<span data-ttu-id="c7302-109">**データ ファイルを閉じませんでした正しく問題の最後に使用されていた、チェックされていること。チェックの実行中に、パフォーマンスは影響を受ける可能性があります。**</span><span class="sxs-lookup"><span data-stu-id="c7302-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="c7302-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7302-110">See also</span></span>

- [<span data-ttu-id="c7302-111">MAPI クラッシュ回復 API について</span><span class="sxs-lookup"><span data-stu-id="c7302-111">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md) 
- [<span data-ttu-id="c7302-112">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="c7302-112">MAPICrashRecovery</span></span>](mapicrashrecovery.md)


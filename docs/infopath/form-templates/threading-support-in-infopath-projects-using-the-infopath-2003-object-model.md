---
title: InfoPath 2003 オブジェクト モデルを使用する InfoPath プロジェクトにおけるスレッドのサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- multithreading [infopath 2007], infopath 2003-compatible form templates,threading [InfoPath 2007], support for projects using InfoPath 2003 object model,InfoPath 2003-compatible form templates, threading support
localization_priority: Normal
ms.assetid: f269d64d-4102-426d-be8e-d2742a993524
description: Microsoft InfoPath によってインストールされる Microsoft.Office.Interop.InfoPath.dll、Microsoft.Office.Interop.InfoPath.SemiTrust.dll、および Microsoft.Office.Interop.InfoPath.Xml.dll 相互運用アセンブリを介してアクセスする COM オブジェクトは、複数のスレッドでの呼び出しをサポートしていません。これには、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間にラップされた Microsoft XML Core Services (MSXML) オブジェクト用インターフェイス (ほとんどの名前に IXMLDOM というプレフィックスが付いています)、および Microsoft.Office.Interop.InfoPath.Xml 名前空間によって公開されるすべてのインターフェイスが含まれており、これらのインターフェイスはどちらもスレッド セーフでありません。
ms.openlocfilehash: 314ef57e11295c0b2dbc9866c5faa392aab055ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799212"
---
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a><span data-ttu-id="055a7-105">InfoPath 2003 オブジェクト モデルを使用する InfoPath プロジェクトにおけるスレッドのサポート</span><span class="sxs-lookup"><span data-stu-id="055a7-105">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="055a7-106">Microsoft InfoPath によってインストールされる Microsoft.Office.Interop.InfoPath.dll、Microsoft.Office.Interop.InfoPath.SemiTrust.dll、および Microsoft.Office.Interop.InfoPath.Xml.dll 相互運用アセンブリを介してアクセスする COM オブジェクトは、複数のスレッドでの呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="055a7-106">The COM objects accessed through the Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll, and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies installed by Microsoft InfoPath do not support calls made on multiple threads.</span></span> <span data-ttu-id="055a7-107">これにより、Microsoft XML Core Services (MSXML) オブジェクトは、(ほとんどの場合は IXMLDOM が付いている名前がある)、 **Microsoft.Office.Interop.InfoPath.SemiTrust**名前空間によって公開されるインターフェイスのすべてをラップするためのインターフェイスが含まれます。[Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/ja-jp/library/microsoft.office.interop.infopath.xml)名前空間、どれもはスレッド セーフであります。</span><span class="sxs-lookup"><span data-stu-id="055a7-107">This includes the interfaces for Microsoft XML Core Services (MSXML) objects that are wrapped by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace (most of which have names that are prefixed with IXMLDOM) and all of the interfaces exposed by the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/ja-jp/library/microsoft.office.interop.infopath.xml)  namespace, none of which are thread-safe.</span></span> 
  
<span data-ttu-id="055a7-p103">これらの COM オブジェクトへのすべての呼び出しは、単一のスレッドから行う必要があります。InfoPath プロジェクトのマネージ コードは他のスレッドを作成してバックグラウンド処理を実行できますが、メイン以外のスレッドで実行されているコードから InfoPath オブジェクト モデルを呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="055a7-p103">All calls made to these COM objects must be issued on a single thread. Managed code in an InfoPath project can create other threads to perform background work, but code running on threads other than the main thread cannot call into the InfoPath object models.</span></span>
  
<span data-ttu-id="055a7-p104">InfoPath マネージ コード プロジェクトで複数のスレッドを使用する場合は、スレッド間でのオブジェクトの共有に注意する必要があります。XML Document Object Model (DOM) への参照、または InfoPath オブジェクトへの参照は、スレッド間で共有しないでください。</span><span class="sxs-lookup"><span data-stu-id="055a7-p104">If your InfoPath managed code project uses multiple threads, you must be careful about sharing objects between threads. No references to the XML Document Object Model (DOM) or references to InfoPath objects should be shared between threads.</span></span> 
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a><span data-ttu-id="055a7-112">InfoPath オブジェクト モデルに非同期の呼び出しを行う</span><span class="sxs-lookup"><span data-stu-id="055a7-112">Making Asynchronous Calls to the InfoPath Object Model</span></span>

<span data-ttu-id="055a7-113">別のスレッドで動作しているタイマーなどのプロセスを呼び出す必要がある場合、InfoPath オブジェクト モデルがそのような呼び出しをサポートしていないという事実を回避することは可能です。</span><span class="sxs-lookup"><span data-stu-id="055a7-113">For situations where it is necessary to call into a process such as a timer running on a separate thread, it is possible to work around the fact that the InfoPath object model does not support such calls.</span></span> 
  
<span data-ttu-id="055a7-114">次の例では、フォームの _Startup メソッドで **System.Timers.Timer** インスタンスを作成し、タイマーへの非同期コールバックをフックします。</span><span class="sxs-lookup"><span data-stu-id="055a7-114">The following example creates a **System.Timers.Timer** instance in the _Startup method of the form and hooks up an asynchronous callback to the timer.</span></span> <span data-ttu-id="055a7-115">また、window フォーム (**System.Windows.Forms.Form**) の非表示のインスタンスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="055a7-115">In addition, an invisible instance of the window form (**System.Windows.Forms.Form**) is created.</span></span> <span data-ttu-id="055a7-116">タイマーがタイムアウトすると、コールバック関数が 1 秒に 1 回実行されるようになり、Win32 の **PostMessage** 関数を呼び出して非表示のウィンドウにメッセージを送ります。</span><span class="sxs-lookup"><span data-stu-id="055a7-116">When the timer elapsed callback function executes once per second, it calls into the Win32 **PostMessage** function to post a message to the invisible window.</span></span> <span data-ttu-id="055a7-117">非表示のウィンドウには、タイマー コールバック関数から受け取ったメッセージを処理し、フォームの XML Document Object Model (DOM) を更新する **WndProc** 関数があります。</span><span class="sxs-lookup"><span data-stu-id="055a7-117">The invisible window has a **WndProc** function that processes the message it receives from the timer callback function, and updates the XML document object model (DOM) of the form.</span></span> <span data-ttu-id="055a7-118">このフォームを実行するには、完全に信頼できるフォームとしてインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="055a7-118">This form must be installed as a fully trusted form to run.</span></span> <span data-ttu-id="055a7-119">完全に信頼されたフォーム テンプレートをデバッグする方法の詳細については、[プレビューしその必要とする完全信頼フォーム テンプレートのデバッグ](how-to-preview-and-debug-form-templates-that-require-full-trust.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="055a7-119">For information on debugging a fully trusted form template, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> <span data-ttu-id="055a7-120">完全に信頼されたフォーム テンプレートを展開する方法の詳細については、[コードを含む InfoPath フォーム テンプレートの展開](how-to-deploy-infopath-form-templates-with-code.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="055a7-120">For information on deploying a fully trusted form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
using System.Timers;
using System.Runtime.InteropServices;
// Office integration attribute. Identifies the startup class for the
// form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute("InfoPathStartupClass, Version=1.0, Class=AsyncUpdate.AsyncUpdate")]
namespace AsyncUpdate
{
    public class User32
    {
        [DllImport("User32.dll")]
        public static extern Int32 PostMessage(
            IntPtr hWnd, int Msg, int wParam, int lParam);
        public User32()
        {    
        }
        ~User32()
        {
        }
    }
    public class MyWindow : System.Windows.Forms.Form
    {
        private XDocument thisXDocument;
        private AsyncUpdate thisProcess ;
        // Private message for internal class.
        public const int WM_MYNOTIFY = 0x400;
        public MyWindow(XDocument doc, AsyncUpdate process)
        {
            thisXDocument = doc;
            thisProcess  = process;
            this.Text = "MyWindow";
            // Force HWND to get created in Win32
            IntPtr hwnd = this.Handle; 
        }
        [System.Security.Permissions.PermissionSet(System.Security.Permissions.SecurityAction.Demand, Name="FullTrust")]
        protected override void WndProc(
            ref System.Windows.Forms.Message m) 
        {
            switch (m.Msg)
            {
            case WM_MYNOTIFY:
                IXMLDOMNode xml = thisXDocument.DOM.selectSingleNode(
                    "/my:myFields/my:field1");
                xml.text = thisProcess.counter.ToString();
                break;                
            }
            base.WndProc(ref m);
        }
    }
    // The namespace prefixes defined in this attribute must remain 
    // synchronized with those in the form definition file (.xsf).
    [InfoPathNamespace("xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-02-11T23-29-59'")]
    public class AsyncUpdate
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public int counter;
        private System.Timers.Timer myTimer;
        private MyWindow myWnd;
    
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // init the counter
            counter = 0;
            // Start a timer on another thread
            myTimer = new System.Timers.Timer(1000);
            myTimer.Elapsed += new ElapsedEventHandler(
                myTimer_Elapsed);
            myTimer.Start();
            // create hidden window to receive notifications 
            // back on the main thread
            myWnd = new MyWindow(thisXDocument, this);
        }
        public void _Shutdown()
        {
            myWnd.Dispose();
            myTimer.Stop();
            myTimer.Dispose();
        }
        private void myTimer_Elapsed(object sender, ElapsedEventArgs e)
        {
            // This method is called on a second thread
            counter ++;
            // Post message back to main thread
            User32.PostMessage(
                myWnd.Handle, MyWindow.WM_MYNOTIFY, 0, 0);
        }
    }
}

```



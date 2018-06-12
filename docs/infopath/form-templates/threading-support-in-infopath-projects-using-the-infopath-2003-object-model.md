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
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用する InfoPath プロジェクトにおけるスレッドのサポート

Microsoft InfoPath によってインストールされる Microsoft.Office.Interop.InfoPath.dll、Microsoft.Office.Interop.InfoPath.SemiTrust.dll、および Microsoft.Office.Interop.InfoPath.Xml.dll 相互運用アセンブリを介してアクセスする COM オブジェクトは、複数のスレッドでの呼び出しをサポートしていません。 これにより、Microsoft XML Core Services (MSXML) オブジェクトは、(ほとんどの場合は IXMLDOM が付いている名前がある)、 **Microsoft.Office.Interop.InfoPath.SemiTrust**名前空間によって公開されるインターフェイスのすべてをラップするためのインターフェイスが含まれます。[Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml)名前空間、どれもはスレッド セーフであります。 
  
これらの COM オブジェクトへのすべての呼び出しは、単一のスレッドから行う必要があります。InfoPath プロジェクトのマネージ コードは他のスレッドを作成してバックグラウンド処理を実行できますが、メイン以外のスレッドで実行されているコードから InfoPath オブジェクト モデルを呼び出すことはできません。
  
InfoPath マネージ コード プロジェクトで複数のスレッドを使用する場合は、スレッド間でのオブジェクトの共有に注意する必要があります。XML Document Object Model (DOM) への参照、または InfoPath オブジェクトへの参照は、スレッド間で共有しないでください。 
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a>InfoPath オブジェクト モデルに非同期の呼び出しを行う

別のスレッドで動作しているタイマーなどのプロセスを呼び出す必要がある場合、InfoPath オブジェクト モデルがそのような呼び出しをサポートしていないという事実を回避することは可能です。 
  
次の例では、フォームの _Startup メソッドで **System.Timers.Timer** インスタンスを作成し、タイマーへの非同期コールバックをフックします。 また、window フォーム (**System.Windows.Forms.Form**) の非表示のインスタンスが作成されます。 タイマーがタイムアウトすると、コールバック関数が 1 秒に 1 回実行されるようになり、Win32 の **PostMessage** 関数を呼び出して非表示のウィンドウにメッセージを送ります。 非表示のウィンドウには、タイマー コールバック関数から受け取ったメッセージを処理し、フォームの XML Document Object Model (DOM) を更新する **WndProc** 関数があります。 このフォームを実行するには、完全に信頼できるフォームとしてインストールする必要があります。 完全に信頼されたフォーム テンプレートをデバッグする方法の詳細については、[プレビューしその必要とする完全信頼フォーム テンプレートのデバッグ](how-to-preview-and-debug-form-templates-that-require-full-trust.md)を参照してください。 完全に信頼されたフォーム テンプレートを展開する方法の詳細については、[コードを含む InfoPath フォーム テンプレートの展開](how-to-deploy-infopath-form-templates-with-code.md)を参照してください。
  
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



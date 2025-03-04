---
title: "Encoding and Windows Forms Globalization"
ms.date: "03/30/2017"
helpviewer_keywords:
  - "ListView control [Windows Forms], lack of Unicode support"
  - "DateTimePicker control [Windows Forms], lack of Unicode support"
  - "TrackBar control [Windows Forms], lack of Unicode support"
  - "ImageList component [Windows Forms], lack of Unicode support"
  - "Unicode [Windows Forms]"
  - "ToolBar control [Windows Forms], lack of Unicode support"
  - "international applications [Windows Forms], character display"
  - "StatusBar control [Windows Forms], lack of Unicode support"
  - "MonthCalendar control [Windows Forms], lack of Unicode support"
  - "international characters"
  - "TabControl control [Windows Forms], lack of Unicode support"
  - "Windows Forms, encoding"
  - "TreeView control [Windows Forms], lack of Unicode support"
  - "ProgressBar control [Windows Forms], Unicode-enabled forms"
  - "localization [Windows Forms], character sets"
  - "globalization [Windows Forms], character sets"
ms.assetid: 22e8965d-a712-42b3-8167-3ee346bd70f9
---
# Encoding and Windows Forms Globalization

Windows Forms applications are entirely Unicode-enabled, meaning that each character is represented by a unique number, no matter what the platform, program, or language. For more information about Unicode, see the [Unicode consortium Web site](https://www.unicode.org).

## Benefits of Unicode

The benefits of Unicode-enabled forms include the ability to work with scripts that are Unicode-only, such as Hindi. In addition, you can use multiple languages on a single form. In Unicode, all characters are two bytes long, so no special effort is needed to represent double-byte characters. You can also write a single set of code that will work on all platforms. This is a change from previous versions of Visual Basic, in which you had to write different code for different platforms, such as Windows NT and Windows 98.

However, certain controls do not support Unicode in Windows 98 and Windows Millennium Edition. These controls, all of which inherit from the common control, will process data with the Windows code pages, as ANSI. These controls are: <xref:System.Windows.Forms.TabControl>, <xref:System.Windows.Forms.ListView>, <xref:System.Windows.Forms.TreeView>, <xref:System.Windows.Forms.DateTimePicker>, <xref:System.Windows.Forms.MonthCalendar>, <xref:System.Windows.Forms.TrackBar>, <xref:System.Windows.Forms.ProgressBar>, <xref:System.Windows.Forms.ImageList>, <xref:System.Windows.Forms.ToolBar>, and <xref:System.Windows.Forms.StatusBar>. As a result, you cannot display Unicode data in these controls on the listed platforms. For example, you cannot display Japanese characters on an English Windows 98 operating system.

For Unicode-aware alternatives to the <xref:System.Windows.Forms.ToolBar> and <xref:System.Windows.Forms.StatusBar> controls, use the <xref:System.Windows.Forms.ToolStrip> and <xref:System.Windows.Forms.StatusStrip> controls, which replace these older controls. To maintain a similar look and feel between visual elements in your application, use the <xref:System.Windows.Forms.MenuStrip> control for rendering menus instead of <xref:System.Windows.Forms.MainMenu>. Like <xref:System.Windows.Forms.ToolStrip> and <xref:System.Windows.Forms.StatusStrip>, <xref:System.Windows.Forms.MenuStrip> can also process and display Unicode characters.

## See also

- [Globalizing Windows Forms applications](globalizing-windows-forms.md)

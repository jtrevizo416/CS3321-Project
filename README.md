# CS3321-Project

# Project Name
Learning Management System

Group Members:
* Augustus Newman
* David Dillion
* Deepa Baral
* Joel Trevizo

## Inspiration
Inspired by our former UHD regestration and student information site.

## Table of contents
* [General info](#general-info)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)

## General info
 This is our creation of a Learning Management System that may help ease student to college conection. 
   
 Here we have provided a login that way allow student to access their 

## Setup
  The .zip files have all of the visual studio codes and access file ready.

  If you would like to copy and paste parts of our code please feel free to click on the project tabs.

## Code Examples
 Example of usage:
 
 Public Class Form1
    Private Sub Label1_Click(sender As Object, e As EventArgs) Handles Label1.Click

    End Sub

    Private Sub Student_InfoBindingNavigatorSaveItem_Click(sender As Object, e As EventArgs)
        Me.Validate()
        Me.Student_InfoBindingSource.EndEdit()
        Me.TableAdapterManager.UpdateAll(Me.Student_InformationDataSet)

    End Sub

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        'TODO: This line of code loads data into the 'Student_InformationDataSet.Student_Info' table. You can move, or remove it, as needed.
        Me.Student_InfoTableAdapter.Fill(Me.Student_InformationDataSet.Student_Info)

    End Sub

    Private Sub btnAddStudent_Click(sender As Object, e As EventArgs) Handles btnAddStudent.Click
        Me.Student_InfoBindingSource.AddNew() 'Add Student Information to the Database
        Me.Student_InfoBindingSource.EndEdit()
        Me.Student_InfoTableAdapter.Update(Student_InformationDataSet.Student_Info) 'Save Changes to the student info database
        MessageBox.Show("Student has been succesfully added.")
        'Clear info from the text boxes
        IndexTextBox.Text = ""
        Student_IDTextBox.Text = ""
        First_NameTextBox.Text = ""
        Last_NameTextBox.Text = ""
        Date_Of_BirthTextBox.Text = ""
        GenderTextBox.Text = ""
        PasswordTextBox.Text = ""
    End Sub

    Private Sub btnDeleteStudent_Click(sender As Object, e As EventArgs) Handles btnDeleteStudent.Click
        Me.Student_InfoBindingSource.RemoveCurrent() 'Remove Student from the database
        Me.Student_InfoBindingSource.EndEdit()
        Me.Student_InfoTableAdapter.Update(Student_InformationDataSet.Student_Info) 'save changes made
        MessageBox.Show("Student has been successfully removed")
    End Sub
End Class

## Features
* GPA Calculator
* Add, Delete, Update, and Save from Access to Visual Basic

To-do list:
* Combine student and admin views into one file
* Reduce student view to not show courses available that have already been taken

## Status
Working version 2.01 has been added

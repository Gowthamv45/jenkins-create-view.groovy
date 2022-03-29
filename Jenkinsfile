#!groovy

// imports
import jenkins.model.Jenkins
import hudson.model.MyView
import hudson.views.BuildStatusFilter

// get Jenkins instance
Jenkins jenkins = Jenkins.getInstance()

// variables
def viewName = 'MyView'

// create the new view
jenkins.addView(new MyView(viewName))

// get the view
myView = hudson.model.Hudson.instance.getView(viewName)

List<BuildStatusFilter> expectedFilters = new ArrayList<BuildStatusFilter>()
def filter = new BuildStatusFilter(true,false,false,"includeMatched")
myView.getJobFilters().add(filter)

// add a job by its name
//myView.doAddJobToView('MyJob1')
//myView.doAddJobToView('MyJob2')
//myView.doAddJobToView('MyJob3')

// save current Jenkins state to disk
jenkins.save()

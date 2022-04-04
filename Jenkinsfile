#!groovy

// imports
import jenkins.model.Jenkins
import hudson.model.ListView
//import hudson.views.BuildStatusFilter
import hudson.views.StatusFilter
def signature = 'new groovy.json.JsonSlurperClassic'
org.jenkinsci.plugins.scriptsecurity.scripts.ScriptApproval.get().approveSignature(signature)

// get Jenkins instance
Jenkins jenkins = Jenkins.getInstance()

// variables
def viewName = 'Programview7'

// create the new view
jenkins.addView(new ListView(viewName))

// get the view
myView = hudson.model.Hudson.instance.getView(viewName)

//List<BuildStatusFilter> expectedFilters = new ArrayList<BuildStatusFilter>()
//def filter = new BuildStatusFilter(true,false,false,"includeMatched")
def filter = new StatusFilter(true)
myView.getJobFilters().add(filter)

// add a job by its name
//myView.doAddJobToView('MyJob1')
//myView.doAddJobToView('MyJob2')
//myView.doAddJobToView('MyJob3')

// save current Jenkins state to disk
jenkins.save()


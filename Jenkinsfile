#!groovy

// imports
import jenkins.model.Jenkins
import hudson.model.ListView
import hudson.views.BuildStatusFilter
import hudson.views.JobStatusFilter
//import hudson.views.StatusFilter
//def signature = 'new groovy.json.JsonSlurperClassic'
//org.jenkinsci.plugins.scriptsecurity.scripts.ScriptApproval.get().approveSignature(signature)

// get Jenkins instance
Jenkins jenkins = Jenkins.getInstance()

// variables
def viewName = 'Programview10'

// create the new view
jenkins.addView(new ListView(viewName))

// get the view
myView = hudson.model.Hudson.instance.getView(viewName)

//List<BuildStatusFilter> expectedFilters = new ArrayList<BuildStatusFilter>()
//def filter = new BuildStatusFilter(true,false,false,"includeMatched")
//def filter = new StatusFilter(true)
//myView.getJobFilters().add(filter)

//Add jobstatusfilter
//List<JobStatusFilter> expectedFilters = new ArrayList<JobStatusFilter>()
//def filter = new JobStatusFilter(true,false,false,false,"includeMatched")
//myView.getJobFilters().add(filter)

//Add Filter MostRecentJobsFilter
List<TopLevelItem> filtered = new ArrayList<TopLevelItem>(added)
List<TopLevelItem> addedJobs = asList(allJobs.get(2))
def filter = new MostRecentJobsFilter(true)
myView.getJobFilters().add(filter)

// save current Jenkins state to disk
jenkins.save()

